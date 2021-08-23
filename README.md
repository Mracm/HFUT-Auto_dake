# HFUT_Auto_daka
Github_Action的设置

(1)在Github中新建打开项目HFUT_Auto_daka

(2)点击Star先把项目收藏（手动狗头），然后点击Fork的按钮将项目克隆到自己的Github仓库中
![image](https://github.com/Mracm/HFUT-Auto_dake/tree/main/images/1.png)


(3)需要进行如下的设置，第一步对config.json进行编辑,填入需要打卡的学号、密码、打卡地址、邮箱、方糖酱地址设置


设置成功后点击下方Commit changes进行保存


(4)打开submit.py进行编辑第20、21行填入自己的邮箱与邮箱授权码，邮箱授权码查看方式看链接

什么是授权码，它又是如何设置？_QQ邮箱帮助中心

此图片的alt属性为空；文件名为20210823153442.png
修改后点击提交

(5)进行Github Action操作


点击Actions的按钮，再点击右上角的New workflow


点击set up a workflow yourself


删去Edit new file内的所有内容，并把.github/workflows中的test.yml文件里的内容复制到里面后点击Start commit

（其中值得注意的点在于- cron: ‘0 07 * * *指的是07：00UTC国际时间，相当于北京时间15：00，可以自己按照关系设置需要打卡的具体时间）


这样自动打卡项目的Github Action部署就已经完成

具体项目地址请见https://github.com/Mracm/HFUT-Auto_dake

Windows的自动执行任务设置

注：Windows的自动执行任务设置会相对来说稳定性更高，但是有前提要求是需要在打卡时间内，必须保证电脑是开机状态

(1)在 https://github.com/Mracm/HFUT-Auto_dake 下载Code

(2)win+R进入运行，然后输入cmd进行命令窗口，然后执行命令pip install -r requirements.txt,将会自动安装好所执行程序所需要的包，前提是你需要在电脑中先下载好python3.7版本


(3)其中config.json和submit.py的代码修改操作参考Github Action的(3)(4)步骤

(4)右击Auto_daka.bat文件，用文本框打卡进行编辑，修改为正确的执行路径即可


(5)在windows是搜索界面搜索”任务计划程序“，点击右上角创建基本任务，在操作部分选择启动程序，程序脚本窗口选择Auto_daka.bat文件的路径即可，点击完成按钮即可完成任务计划程序的设置

PS：以上内容非原创，借鉴之前大佬开源项目进行修改并添加了一些新功能。
