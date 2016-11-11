### react-native环境的搭建与模拟器的安装

---
本文将主要介绍React Native环境的搭建和有关开发过程中所用模拟的安装与使用。我在安装和使用本模拟器的过程遇到了许多的坑，在解决和整理后，呈现出来，希望可以给大家有所帮助。

![image](http://image.beekka.com/blog/2015/bg2015033101.png)

一.开发前环境的搭建

在确保装了node的情况下，进行相关的环境初始化和搭建

- 安装react-natvie-cli 命令，这样才可以使用react-native的命令，如果网速好的话，安装比较快，如果网速不好的情况，那就比较痛苦了，不成功的话可以多安装几次试试，直到安装成功。安装命令如下：


```
$ npm install -g react-native-cli
```
安装成功之后可以用react-native-cli  -v 验证一下，是否安装成功，若成功则会返回版本号。

- 初始化一个react-native项目，找一个你要创建项目的目录，然后进入到该根目录，执行如下的命令：


```
$ react-native init ReactNativeProject
```
其中，ReactNativeProject表示项目的名称，这个过程是比较缓慢的，需要耐心等待一下。初始化成功之后就可以运行你的项目，但是，先别着急，咱们还没有搭建好运行项目的环境，也就是咱们下来要说的运行环境的搭建。

二.运行与测试

对于运行环境的话，从两个方面进行介绍，一个就是直接拿真机进行运行，这样的话比较省事，直接拿数据线接入或者让手机和电脑在同一局域网内就可以进行运行测试。运行命令如下：


```
$ react-native run-android
```
如果在真机的情况下进行测试，那么，在不出错误的情况下，就会看到，react-native 的一个界面，这个时候，应该非常的兴奋了，接下来你就可以进行你自己工作的开发了。


三.Genymotion安卓模拟器和VirtualBox虚拟机安装、配置、测试

VirtualBox是一个虚拟机软件，它可以在电脑上提供另一个操作系统的运行环境，使多个系统同时运行。Genymotion是一套完整的工具，它提供了Android虚拟环境。但运行其上的安装模拟器时，需要虚拟机的配合，这里选择使用VirtualBox。


1. 所需的工具
- [VirtualBox安装包](https://www.virtualbox.org/wiki/Downloads)（v5.1.8）（必需）

- [Genymotion安装包](https://www.genymotion.com/download/)（v2.72）（不含VirtualBox，推荐）（必需）

- 如果需要其他版本的VirtualBox安装包和Genymotion安装包可以去在它们的官网下载自己需要版本的安装包：[VirtualBox官网](https://www.virtualbox.org/)，[Genymotion官网](https://www.genymotion.com)，下载好安装包后就可以进行相应的安装了。建议安装virtualbox，否则有可能会遇到意想不到的坑。


（一）VirtualBox虚拟机安装

双击安装包就可以进行傻瓜式的安装了，一路下一步，就可以。
![image](http://images2015.cnblogs.com/blog/781564/201606/781564-20160629140104687-480014000.png)

![image](http://images2015.cnblogs.com/blog/781564/201606/781564-20160629140111577-403630827.png)

如上图是安装径的选择，最好不要有带中文的路径，不然有可能也会报一些未知的错误，为了避免给自己找麻烦，所以，最好就别放在带有中文路径的目录下。

![image](http://images2015.cnblogs.com/blog/781564/201606/781564-20160629140118827-1084493264.png)

![image](http://images2015.cnblogs.com/blog/781564/201606/781564-20160629140126749-1521992467.png)

![image](http://images2015.cnblogs.com/blog/781564/201606/781564-20160629140133781-47957850.png)

![image](http://images2015.cnblogs.com/blog/781564/201606/781564-20160629140459140-2036760127.png)

如上，到这个地方时，网会断开，但是你也不用担心，你可以重新连接一下网就好，或者右键网连接，进入网络设置中心，进行设置一下，把 VirtualBox 有关的那个网给禁用了就好了。


（二）Genymotion安卓模拟器安装配置

- Genymotion安装一样很简单，选好安装路径，一路点击下一步就可以。
- 配置（若还没有账号，需要去官网注册一个账号），注册好账号之后，如下：


![image](http://images2015.cnblogs.com/blog/781564/201606/781564-20160629140840484-699965817.png)

![image](http://images2015.cnblogs.com/blog/781564/201606/781564-20160629141056484-1341038268.png)

![image](http://images2015.cnblogs.com/blog/781564/201606/781564-20160629141107296-1108669567.png)

![image](http://images2015.cnblogs.com/blog/781564/201606/781564-20160629141120624-506896665.png)

![image](http://images2015.cnblogs.com/blog/781564/201606/781564-20160629141130952-176267658.png)

- 下载安卓系统镜像：


![image](http://images2015.cnblogs.com/blog/781564/201606/781564-20160629141144077-781915696.png)

![image](http://images2015.cnblogs.com/blog/781564/201606/781564-20160629141154968-2122696884.png)

![image](http://images2015.cnblogs.com/blog/781564/201606/781564-20160629141204984-542946501.png)

- 启动安卓模拟器

选定下载的镜像，点击Start就可以。

模拟启动成功之后，就可以进行和在真机上步骤一样的测试了。


