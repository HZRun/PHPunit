# PHPunit安装 #
## Linux下安装PHPunit ##
<code>
wget https://phar.phpunit.de/phpunit-6.2.phar<br/>
     //下载文件<br/>
chmod +x phpunit-6.2.phar<br/>
     //更改文件权限由644改为755（官方文档这么写的，我觉得不改权限是不是也行？）<br/>
sudo mv phpunit-6.2.phar /usr/local/bin/phpunit

phpunit --version
</code>
## Windows下安装PHPunit ##
1. 为 PHP 的二进制可执行文件建立一个目录，例如 C:\bin
2. 将  ;C:\bin  附加到  PATH  环境变量中
3. 下载 https://phar.phpunit.de/phpunit-6.2.phar 并将文件保存到 C:\bin\phpunit.phar
4. 打开命令行（例如，按 Windows+R » 输入 cmd » ENTER)
5. 建立外包覆批处理脚本（最后得到文件 C:\bin\phpunit.cmd）：
<pre>
 C:\Users\username> cd C:\bin
 C:\bin> echo @php "%~dp0phpunit.phar" %* > phpunit.cmd
 C:\bin> exit
</pre>
6. 新开一个命令行窗口，确认一下可以在任意路径下执行 PHPUnit：
<pre>
C:\Users\usernamephpunit --version   //如果现实PHPUnit的版本就说明已经安装好了
</pre>
