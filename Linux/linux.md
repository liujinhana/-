# ***\*Linux+InternStudio 关卡\****

**1.** ***\*登陆平台\**** 

平台地址：https://studio.intern-ai.org.cn/ 首先打开链接进入InternStudio，完成登录跳转到控制台界面，如下图所示：

![img](/images/wps1.jpg) 

***\*2.创建开发机\**** 

这里选择创建个人开发机，名称自定义，Cuda版本为12.2，资源配置选择10%，时长默认就行。

![img](/images/wps2.jpg) 

## 2. 使用VScode的remote插件进行远程ssh连接 

安装好了VScode之后，可以在点击左侧的扩展页面，在搜索框中输入“SSH”，第一个就是我们要安装的插件，点开它“Install”就可以了。

![img](/images/wps3.jpg) 

安装完成插件以后，点击侧边栏的远程连接图标，在SSH中点击“+”按钮，添加开发机SSH连接的登录命令。

![img](/images/wps4.jpg) 

回到开发机平台，进入开发机页面找到我们创建的开发机，点击SSH连接。

![img](/images/wps5.jpg) 

我们将登录命令复制下来，然后将命令粘贴到弹出的窗口中，最后回车：

![img](/images/wps6.jpg) 

然后在右下角弹出来的提示窗口中点击“连接”就可以远程到开发机中了。

![img](/images/wps7.jpg)![img](/images/wps8.jpg) 

## 3. 端口映射 

我们创建一个hello_world.py文件，在文件中填入以下内容：

![image-20240712143237239](C:\Users\popsmart\AppData\Roaming\Typora\typora-user-images\image-20240712143237239.png)

在运行代码之前，需要先使用pip install gradio==4.29.0命令安装以下依赖包，然后在Web IDE的终端中运行了一个hello_world.py

![img](/images/wps9.jpg) 

运行python程序，在终端左边就有端口映射，当在开发机中新运行了一个端口vscode也会自动检测出来并且询问你是否映射。

![img](/images/wps10.jpg) 

然后在本地浏览器中打开连接就可以看到web ui的界面了

![img](/images/wps11.jpg) 

## 4. 使用conda创建虚拟环境 

**5****.1创建虚拟环境** 我们可以使用conda create -n name python``=3.10创建虚拟环境，这里表示创建了python版本为3.10、名字为name的虚拟环境。创建后，可以在.conda目录下的envs目录下找到。

![img](/images/wps12.jpg) 

**5****.2查看有哪些虚拟环境** 

conda env list 

conda info -e 

conda info --envs

![img](/images/wps13.jpg) 

**5****.3激活与退出虚拟环境** 

当我们创建完虚拟环境后我们可以使用conda activate wuji（名称自定义）命令来激活虚拟环境，如何查看是否切换成功呢？很简单，只需要看base是否变成了创建的虚拟环境的名称。

![img](/images/wps14.jpg) 

导出命令 

\#获得环境中的所有配置 

conda env export --name myenv > myenv.yml 

\#重新还原环境

 conda env create -f myenv.yml

删除虚拟环境命令 

全部删除conda remove --name name --all 

删除指定安装包conda remove --name name package_name

 
