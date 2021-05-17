# roomfrilist
PC微信机器人之实战分析微信获取群好友列表
QQ：2645542961
今天讲一下微信获取群成员列表的功能，首先先找一个群，知道这个群的id，然后附加微信到CE，原理就是点击某个微信群的时候，他会取出该群的所有成员列表信息，当切换点击的时候，CE上面会显示不同的群id，先切换个人的微信，然后搜索wxid_，过滤一些数据。
![image](https://user-images.githubusercontent.com/73727649/118447297-307a6c80-b723-11eb-9086-858bfc15e109.png)
然后切换到某个群，就直接显示某个群的id了，然后记录下来这个群的id，然后再切换到其他群，继续过滤，剩下7条数据了。
![image](https://user-images.githubusercontent.com/73727649/118447327-38d2a780-b723-11eb-84e9-83c471b5f9f1.png)
![image](https://user-images.githubusercontent.com/73727649/118447337-3b350180-b723-11eb-8c67-bb999b47951b.png)
然后把过滤到的，移到下面，然后选择几个修改后面的Value值为另外一个群的id，如果切换后跟着变化，说明就是这个地址，然后复制到OD里面，下断点
![image](https://user-images.githubusercontent.com/73727649/118447546-7fc09d00-b723-11eb-88a5-570f16373ff8.png)
给找到的地址下一个内存访问断点，然后点击一下微信群，他就断下来了，
然后一直走断点找到wxid，
![image](https://user-images.githubusercontent.com/73727649/118447559-85b67e00-b723-11eb-93ab-e007a9a3a235.png)
![image](https://user-images.githubusercontent.com/73727649/118447567-8818d800-b723-11eb-8b99-6658c243de74.png)
目前已经实现了大部分功能，运行稳定，比如：发各种消息，接收各种消息，群管，下载文件，加好友，检测僵尸粉等等功能，可提供接口，方便二次开发，欢迎技术交流。
QQ：2645542961
![image](https://user-images.githubusercontent.com/73727649/118447634-9b2ba800-b723-11eb-932e-5288fcc6bd61.png)
