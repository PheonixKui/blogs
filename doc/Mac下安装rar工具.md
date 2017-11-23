### Mac下安装rar工具
在Mac OS X系统中默认不支持 RAR 文件的解压缩。下面演示如何在Mac OS X系统中使用 rar 命令行操作。  

1. 首先从rarlab 网站下载 rar ／ unrar 工具；  
2. 解压缩下载的 tar.gz 压缩包（rarosx－4.1.0.tar.gz），在下载目录downloads下自动创建一个rar的目录，其中有rar ／ unrar 文件；  
3. 进入命令窗口 － /Applications/Utilities，或者通过Launchpad 进入，如下图所示；

4. 进入刚刚解压缩的rar 目录，使用 cd downloads/rar 进入；
5. 使用如下命令分别安装 unrar 和 rar 命令；

>安装unrar 命令  
>~$: sudo install -c -o $USER unrar /bin  
说明：$USER is a default environment variable in the bash shell which contains your username.
sudo 需要输入password，和你登录到Mac OS X 系统的password一致。  
>>出现错误：install: /bin/rar: Operation not permitted
解决办法：mac 系统一般没有权利修改/bin和/usr/bin目录的，故把上面命令中的/bin改为/usr/local/bin即可。

>下面安装rar 命令：  
~$: sudo install -c -o $USER rar /bin  
6. 测试 unrar 和 rar 命令；  
~$: unrar  
如果 unrar 和 rar 正确安装，则会显示响应的unrar 和 rar 用法。  
~$: unrar x compressed-package.rar  
解压缩 compressed-package.rar 压缩包，如果文件名有空格，则需要使用单引号包起来，如下所示：  
unrar x ‘Sams Teach Yourself iOS 5 Application Development in 24 Hours 3rd Edition.part1.rar’  

