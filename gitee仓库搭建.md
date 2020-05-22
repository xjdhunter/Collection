* 创建gitee仓库

* 设置SSH公钥
``` 
执行命令生成公钥： ssh-keygen -t rsa -C "xxxxx@xxxxx.com"  
生成公钥路径 ： C:\Users\Admin\.ssh
粘贴id_rsa.pub里面的内容到gitte设置里面的公钥中，如果已经存在先删除原来的在添加
```
* 链接本地仓库和远程库
```
 1.右键本地文件夹 git bash here
 2.输入个人信息(代码提交者) ： git config --global user.name "xxxx" 
                           git config --global user.email xxxxx@qq.com
 3.执行 ： git init 生成.git文件
 4.添加代码到暂存区： git add .
 5.把代码上传到本地仓库 ： git commit -m '描述'
 6.关联本地仓库并上传代码：git remote add origin https://github.com/Yanyf765/hr_sys.git（仓库地址）
   可能报以下错误：fatal: remote origin already exists.
   解决办法：手动修改gitconfig文件的内容
   执行：vi .git/config
   把[remote “origin”] 那一行删掉就好了。
   重新关联:git pull origin master --allow-unrelated-histories
 7.上传代码到远程分支：git push origin master
   可能报错：remote: Incorrect username or password ( access token )
   原因：由于之前重置了Git账户的密码，忘记修改计算机的凭据导致这个问题的出现。
   解决：打开电脑的控制面板–>用户账户–>管理Windows凭据 找到普通凭据中自己的账号信息，选择编辑，填入正确的用户名和密码，最后点击保存即可。
 * 下载代码
  ```
  git clone 地址
  ```
 


