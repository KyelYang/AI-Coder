# AI-Coder
AI-Coder是一个面向TensorFlow领域进行智能代码句补全的PyCharm插件。

- backend——对应代码句补全服务器
- plugin——插件开发与配置
- model——代码句预测模型
- dataset——模型训练的数据集

## 服务器
代码句补全服务器使用了两种框架，分别是Flask和Crow。
### flask

#### 1. 准备

如果没有安装 flask，先安装 flask。anaconda 自带了 flask。
`pip install flask`

#### 2. 运行

进入 backend 文件夹，运行 serve.py。

在浏览器中输入 localhost:9078/plugin_test?keyword=helloworld ，浏览器返回内容如下。

<img src="doc/img/backend_helloworld.jpg" width="50%"/>

后端获取 keyword 中的数据，处理之后返回。后续我们使用模型处理输入，道理是一样的。

## Crow
[Crow](https://github.com/ipkn/crow)是一个轻量级的Web服务器框架，这个框架是受Python下的Flask启发的，其实现的功能和Flask基本一致，核心的区别在于Crow是用C++编写的，性能较Flask有一定的提升。


