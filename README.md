## OminiControl（基于 Flux 结构）

### Train

```bash
bash train/script/train_multi_condition.sh
```


## InsertAnything（基于 Flux-Fill 结构）

### Train

```bash
bash scripts/train.sh
```

### inference

```bash
python val_fill.py \
  --input_json ../data/anytext_benchmark/wukong_word/test1k_input.json \
  --output_dir result/fill_wukong \
  --masked_input_dir result/wukong_word \
  --output_jsonl result/fill_wukong.jsonl \
  --glyph_dir ../data/anytext_benchmark/wukong_word/glyph_wukong
```

input_json：输入的 JSON 文件路径

output_dir：生成图像的保存目录

masked_input_dir：masked image保存目录

output_jsonl：结果保存为 JSONL 格式

glyph_dir：字形图像路径


## 数据处理文件说明

### 1. 图像去重 (rm_duplicate.py)

**功能**：去除重复图像文件

**使用方法**：
```bash
python rm_duplicate.py
```
参数说明：

input_dir: 包含图像的子文件夹的根目录

jsonl_files: 包含已有图像信息的jsonl文件列表

output_jsonl: 输出结果的目标jsonl文件

### 2. 美观度打分 (cal_aes.py)
**功能**：计算图像美观度评分

**使用方法**：

```bash
python cal_aes.py
```
参数说明：

input_json: 输入的原始json文件

save_path: 美观度打分后的json文件保存路径

### 3. Caption标注 (client.py)
**功能**：为图像添加caption标注

**使用方法**：

```bash
python client_1.py
```
参数说明：

input_jsonl: 输入的jsonl文件

output_jsonl: caption标注后的jsonl文件保存路径

### 4. OCR标注 (client_pp.py)
**功能**：为图像添加OCR标注

**使用方法**：

```bash
python client_pp_1.py --gpus 8 --gpu_id 0 --input data/input.jsonl --output data/output.jsonl
```
参数说明：

--gpus: 可用的GPU数量

--gpu_id: 使用的GPU ID

--input: 输入jsonl文件路径

--output: 输出jsonl文件路径
