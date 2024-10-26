环境配置：
Ubuntu20.04
Pytorch：2.4.0
Cuda：12.1.1
硬件：NVIDIA GeForce RTX 4090-24G

数据处理：
1.将测试集，A数据集，B数据集均运行{  路径  }gen_modal中的{    }模式，得到处理后的数据集
2.经过gen_model转换后放置于TE-GCN-main下的data文件夹里

训练运行方式：
进入该项目文件夹后，在终端里面运行bash scripts/TRAIN_V1.sh即可

结果复现：
打开work dir文件夹的{   }文件夹，打开log.txt,其中第{  }批次的准确率较高，在run文件夹里的{   }文件夹找到该批次的权重文件，复制该文件路径，修改config/{         }/test.yaml文件中的weight路径，再次在终端里运行bash scripts/EVAL {   }.sh即可得到测试集B的置信度文件。
