git init
git add .
git commit -m "注释内容"   //提交到本地
git remote add origin 远程仓库地址
git push -u origin master -f

git add .
git commit -m ""
git push

### 遇到的错误



错误一：10054
unable to access 'https://github.com/Logical-Ghost/supermall.git/': OpenSSL SSL_read: Connection was reset, errno 10054
产生原因：一般是这是因为服务器的SSL证书没有经过第三方机构的签署，所以才报错
参考网上解决办法：解除ssl验证后，再次git即可解决办法：
打开git bash here 输入 git config --global http.sslVerify "false"

错误二：fatal: remote origin already exists.
解决办法：
1.先删除远程Git仓库
	$ git remote rm origin
2.在添加远程Git仓库
	$ git remote add origin 仓库地址

