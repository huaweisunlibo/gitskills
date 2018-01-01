http://blog.csdn.net/x728999452/article/details/50759249

https://gpg4win.org/download.html

windows下GPG的使用
原创 2016年02月28日 11:16:14 2925
GPG即GNU PrivacyGuard，它是加密工具PGP（Pretty Good Privacy）的非商业化版本，用于对Email、文件及其他数据的收发进行加密与验证，确保通信数据的可靠性和真实性。
一、GPG的安装
下载链接:www.gnupg.org

二、GPG的使用
1.生成密钥对，在命令行输入如下命令：
gpg --gen-key
系统将询问名称、电子邮箱，输入完成后将弹出对话框

输入Passphrase（必须提供，解密是需要，如果私钥被盗，将无法使用）。

2.列出公钥，在命令行输入如下命令：
gpg --list-keys

3.导出公钥，在命令行输入如下命令：
gpg --export -armor -o filename(文件目录如  F:\file.txt)
或者
gpg --export -a > filename
将公钥导出至文件，以便于其他人使用。
-armor选项（同-a选项）以文本形式显示输出，而非二进制格式。

4.导入公钥，在命令行输入如下命令：
gpg --import filename
 
导入其他人的公钥

5.加密文件，在命令行输入如下命令：
gpg --encrypt -armor -r key-id filename
用key-id的公钥加密消息。如果未提供-r key-id，命令将提示收件人输入。默认输出文件为filename.asc。

6.解密文件，在命令行输入如下命令：
gpg --output 新文件名 --decrypt 加密文件名
将会提示输入Passphrase。

7.修改密钥，在命令行输入如下命令：
gpg --edit-key 标识名

8.删除密钥，在命令行输入如下命令：
必须先删除私钥，然后才能删除公钥。
在命令行输入如下命令：
gpg --delete-secret-keys 标识名
gpg --delete-keys 标识名