## 文件说明

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

###2. 美观度打分 (cal_aes.py)
**功能**：计算图像美观度评分

**使用方法**：

```bash
python cal_aes.py
```
参数说明：

input_json: 输入的原始json文件

save_path: 美观度打分后的json文件保存路径

###3. Caption标注 (client.py)
**功能**：为图像添加caption标注

**使用方法**：

```bash
python client_1.py
```
参数说明：

input_jsonl: 输入的jsonl文件

output_jsonl: caption标注后的jsonl文件保存路径

###4. OCR标注 (client_pp.py)
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
