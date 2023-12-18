# deep-learning-model
记录做过的深度学习项目

## Github Structure:
- DPR Model: 气象科学内容自动识别模型，
- Image similarity comparison model: 图像相似度比较模型，
- Instruct Learning GPT2: 指示学习微调GPT2模型，

## ChangeLog
| Version | Release Date | Changes |
| ------- | ------------ | ------- |
| 1.0 | 2/20/2023 | <ul><li>nlp任务数据收集</li><li>GPT2 model 训练</li></ul> |
| 2.0 | 7/2/2023 | <ul><li>数据预处理（正负采样）</li><li>Bert model 训练</li></ul> |
| 3.0 | 10/20/2023 | <ul><li>数据预处理（正负采样，数据增强）</li><li>VGG16/Resnet50 model 训练</li></ul> |

## 指示学习微调GPT2模型
独立微调GPT2的模型（用的是Huggingface网站上的Wenzhong-GPT2的预训练模型）。同时负责nlp任务相关数据（以百度千言数据库里的资源为主）的收集与预处理（文本总结，中英互译，QA问答，文本分类）。这个工作的主要目的是通过指示学习的数据预处理的方式，提升GPT2模型的性。 

## 气象科学内容自动识别模型
模型需要完成的任务有两个。第一个任务是文本检索,该模型是基于DPR(Dense Passage Retrieval)模型的理论复现，根据数据集中的一百万条evidnece中找到和给定的question最相关的几条信息。第二个任务是理解evidence和question的内容去进行文本分类（分类的类型有四种：支持，反对，有争议，没有足够的证据）。最后算出找到的文本和分类的正确率评估模型的性能。

## 图像相似度对比模型
设计了一个可以接近人类感知相似度的算法模型（采用了Resnet和VGG两个预训练模型）去比较两张图片的相似性。模型的结构和损失函数有创新性的设计，同时采用了数据增强和正负采样的数据预处理方法以提高模型的泛化能力。模型的验证准确率达到了课程内kaggle比赛的前20%。
