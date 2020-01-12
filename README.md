# pytorch_ERNIE_Intention

# requirement
- torchvision >=0.4.2
# 预训练模型
- 训练前，需先在release页面中下载ERNIE预训练模型
- release地址： [https://github.com/BUAA-Umetrip-cooperation/Intention_Classification/releases/download/1.0/pretrained_ERNIE.zip]
- 在当前目录下解压，文件夹名为pytrained_ERNIE，文件夹内有三个文件： `bert_config.json
  pytorch_model.bin vocab.txt`

# LABEL_TO_ID
- 文件utils/constant.py的LABEL_TO_ID常量，是有数据的单级类别与id的对应关系
- **训练前需根据数据情况，修改文件内容**

# Train
> sh train_Grained.sh 

- 部分参数说明：
    -  data_dir：数据集目录
    -  ERNIE_dir：ERNIE预训练模型所在目录
    -  input_dropout：默认0.4 若训练效果不佳，可调节该参数
