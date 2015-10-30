#2015-10-29
##从本地建立与github的连接
###一、环境
1. yum install git 4.2
2. yun install openssh
###二、本地仓库
1. 建立一个文件夹 ~/github
2. 创建ssh联系
  - ssh-keygen -t rsa -C "lidongshengluck@163.com"
  - 键入文件名x
  - 键入密码xiaomihu24
  - 把生成的x.pub的内容复制给github个人帐号setting里的sshkey，创建一个新密钥
  - 把刚才生成的x和x.pub复制并覆盖到~/.ssh/下的id_rsa,id_rsa.pub中
  - 然后把x删了ok
3. 现在可以克隆了，git clone httpurl
4. git config --global user.name 'lidongshengluck'
5. git config --global user.email 'lidongshenglucd@163.com'
6. touch readme
7. git init
8. 可切换到你想上传到的文件夹下cd lidongshengluck.github.in/_posts/
9. vi a.md
10. git add a.md
11. git commit
12. git push 输入lidongshengluck和密码xiaomihu24
13. 上传成功
###三、本地删除
1. git rm xxx
2. git add .
3. git commit
4. git push
###四、常用
- add
- commit
