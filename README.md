   

注意事项：

1.请把train和val一起放在/dataset/MTFood-1000/data/train文件夹下，一共是85296张图片，test单独放在/dataset/MTFood-1000/data/test里

2.labels已经制作好了，注意那个test_lable.txt没有用，但不要删，如果要再次制作label需要删除以前的txt

3.我是在两块1080ti上训练的，大概30个epoch用了15个小时，根据自己服务器情况调整train.py里batch和numworkers

4.resnet50的预训练模型已经放在了moels里，其它模型的话请看config.py，并修改train.py相关参数

5.我设置的每1000个step评估一次val，并保存模型，没有评估train，print的信息被我改的比较混乱，重点看train的三个loss和val的top3_acc，可以自行修改

6.pytorch用的是0.4.0

7.训练直接运行train.py，验证val运行val.py，预测运行test.py，注意修改val.py和test.py的108行为自己训练保存的模型，运行完后手动将xls转为csv.

