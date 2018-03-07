**在虚拟机中的Linux配置Java**：

从windows中下载linux环境下的java安装包。  
在虚拟机中设置共享文件夹。 （具体看教程）   
将安装包拷贝至共享文件夹中。  
将共享文件夹中的安装包拷贝到你自己定义的文件夹中。例如：  
cp -r /mnt/hgfs/VmWithWindow/* /home/liujian/user/jdk/
拷贝/mnt/hgfs/VmWithWindow 下的所有文件到 /home/liujian/user/jdk中去。  
安装。  
设置环境变量：  

·用文本编辑器vim打开/etc/profile  sudo vim /etc/profile（或者提前切换到root,前面不需要加上sudo了：
su root 获取root用户权限，当前工作目录不变。）   
·在profile文件末尾加入：   
export JAVA_HOME=/usr/share/jdk1.6.0_14(此处注意要是你自己的文件位置路径)   
export PATH=$JAVA_HOME/bin:$PATH   
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/  tools.jar 

保存和退出需要了解vim文本编辑器的一些基本操作。
**vim的使用方法大致了解一下，否则会走一些弯路。**
