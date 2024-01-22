1、安装git和tortoisegit
2、安装tortoisegit时设置其中的name和email为GitHub账户
3、在本地中生成ssh的公钥和私钥
4、在使用tortoisegit时需要修改设置中的网络部分中的SSH客户端为：C:\Program Files\Git\usr\bin\ssh.exe。也就是git自身的ssh
5、把本地生成的ssh公钥设置到GitHub账户中
6、此时，可以使用tortoisegit拉取代码，也就是克隆功能
7、本地修改之后可以提交后推送到远程GitHub。如果GitHub上修改了可以拉取新的
8、如果上面的克隆失败，则需要在.ssh目录中创建config文件，然后加入以下内容：
				Host github.com
				HostName ssh.github.com  # 这是最重要的部分
				User git
				Port 443
				PreferredAuthentications publickey
				IdentityFile ~/.ssh/id_rsa
