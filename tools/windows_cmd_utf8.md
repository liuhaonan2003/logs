# windows cmd命令显示UTF8设置

在中文Windows系统中，如果一个文本文件是UTF-8编码的，那么在CMD.exe命令行窗口（所谓的DOS窗口）中不能正确显示文件中的内容。在默认情况下，命令行窗口中使用的代码页是中文或者美国的，即编码是中文字符集或者西文字符集。 


如果想正确显示UTF-8字符，可以按照以下步骤操作： 

1、打开CMD.exe命令行窗口 

2、通过 chcp命令改变代码页，UTF-8的代码页为65001 

chcp 65001 

执行该操作后，代码页就被变成UTF-8了。但是，在窗口中仍旧不能正确显示UTF-8字符。 

3、修改窗口属性，改变字体 

在命令行标题栏上点击右键，选择"属性"->"字体"，将字体修改为True Type字体"Lucida Console"，然后点击确定将属性应用到当前窗口。 

这时使用type命令就可以显示UTF-8文本文件的内容了： 

type filename.txt 

4、通过以上操作并不能完全解决问题，因为显示出来的内容有可能不完全。可以先最小化，然后最大化命令行窗口，文件的内容就完整的显示出来了。

转自：http://www.cnblogs.com/QQParadise/articles/1685177.htm
 


转成utf-8 运行python遇到以下问题：

# python交互模式下cp65001异常
unknown encoding: cp65001异常
python安装后进入命令行交互模式，输入任何代码都报unknown encoding: cp65001异常

需要将编码(UTF-8)修改为 简体中文(GBK)
 在CMD窗口执行　chcp 936

转自： http://blog.csdn.net/ahywg/article/details/23442867