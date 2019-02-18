# Atomy配置python环境

## 安装python

[传送门](https://www.python.org/)

## 安装Atom

[传送门](https://atom.io/)

## 安装script插件

atom安装插件可以说是很费事了，因为被墙，安装速度特别慢，甚至安装不上。因此我将源修改为淘宝的，打开cmd（可以通过使用win+R打开运行窗口后输入cmd来打开cmd）
```
apm config set registry https://registry.npm.taobao.org  
```

然而并没有什么卵用，还是安装不了。

这个时候就要重新选择一种方法，手动安装。在[github](https://github.com/rgbkrk/atom-script)上下载该插件，解压到atom安装目录下的packages文件夹，然后打开cmd，执行`npm install script`就可以看到如下图所示（如果显示npm不是内部命令，则需要安装node.js。安装教程c某dn一大堆，就不在这里介绍了）

![](https://cloud-minapp-15476.cloud.ifanrusercontent.com/1gvcBc96tbLFGiM5.png)

这里有一些警告，不要在意这些细节，只要我们看到下面的+ script@x.x.x就说明安装成功了。重新打开Atom，![](https://cloud-minapp-15476.cloud.ifanrusercontent.com/1gvcBcgsRFuYP1On.png)

插件就有了。

你以为这就完事了吗，想都不用想，肯定有坑。新建一个python文件，输入几行能运行的代码。例如：

`print ("Hello, Python!")`（这是pythom3.x的语法，如果你安装的是2.x，print的内容不需要加括号）然后使用快捷键Ctrl+Shift+P，输入run会显示如下界面

![](https://cloud-minapp-15476.cloud.ifanrusercontent.com/1gvcFJs4YyYnLqo6.png)

点击第一个，

![](https://cloud-minapp-15476.cloud.ifanrusercontent.com/1gvcBcBa7whuiMfv.png)

看，报错了吧。坑是无处不在的。错误信息是没有找到uuid包，那就给它安装一个。打开cmd，进入atom安装目录下的packages目录，具体怎么进入请看下图，然后执行`npm install uuid`

![](https://cloud-minapp-15476.cloud.ifanrusercontent.com/1gvcWJvRhOBOaRsZ.png)

我这进入目录是一层一层进的，有点智障。安装好之后再试一下run，还是会报错，找不到各种各样的模块，按照上面的方法一个一个安装就好了。然后我按照提示安装了下面这一堆模块。

![](https://cloud-minapp-15476.cloud.ifanrusercontent.com/1gvcBcDeOnrHTGV7.png)

全部安装好之后，终于可以运行了！

![](https://cloud-minapp-15476.cloud.ifanrusercontent.com/1gvcg3ZiB38iYCeO.png)

