# Seal-OCR-For-BLAR
“国土资源国土资源智能文档解析系统”项目

## 背景/需求
- OCR输入PDF文档正文内容。
- OCR所盖公章上面的文字，与公章下面的落款单位对比，如果一致则通过，不一致则提示用章错误，转为人工处理。
## 环境需求
-   Windows or Linux
-   Python >= 3.5
-   Pillow >= 6.1.0
-   torch >= 1.2.0
-   torchvision >= 0.4.1
-   opencv-python >= 4.2.0
-   scikit-image >= 0.17.2
-   scipy >= 1.3.1
-   cuda >= 10.0
-   Full conda list can be found in environment.txt and craft/requirements.txt

## 代码目录结构
```
├── CRAFT(弯曲文本检测模型)
│   ├── basenet
│   ├── data(印章原始数据)
│   ├── fail_log(用于保存后处理过程中出现的异常)
│   ├── polar-img(仿射矫正后的正常语序印章文本)
│   ├── result(CRAFT模型原始检测结果)
│   ├── imgproc.py(包含自定义后处理，实现根据result文件夹中的原始输出，经处理生成polar-img中的仿射矫正后的正常语序印章文本)
├── TPS(模糊文本识别模型)
├── creat_dataset(用于生成合成数据集，训练TPS模型)
```
## 项目技术方案
