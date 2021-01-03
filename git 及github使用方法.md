# git 及github使用方法

1. 创建一个github账号以及一个新的文件路径
2. 在本地运用`ssh-keygen -t rsa_name -C "your_email@youremail.com"`创建一个指向github的密钥，其中`rsa_name`是密钥的名字，而`your_emain@youremail.com`是创建github的用户邮箱
3. 在`~/.ssh`里面找到`rsa_name.pub`里面的内容把它复制下来
4. 到github个人的设置里面找到`ssh key`设置，添加key, 在对话框里把第3步复制下来的内容给粘贴上去![image-20210104011808350](/home/yangyue/.config/Typora/typora-user-images/image-20210104011808350.png)
5. 将`~/.ssh/rsa_name`文件用`chmod 600`命令修改一下文件权限
6. 使用`ssh -T git@github.com `来验证是否登录成功，出现`You've successfully authenticated, but GitHub does not provide shell access`说明登录成功了
7. 进入相关的目录，运行`git init` 将当前的目录变成git仓库。里面会有一个.git文件
8. 运行`git config --global user.name "your name"`和 ` git config --global user.email "your_email@youremail.com"`两条命令，将github的用户名和邮箱添加到当前的文件夹的下
9. 之后`git remote add origin git@github.com:yourName/yourRepo.git`将需要与当前文件夹相关联（即上传和下载的）远程路径地址添加到.git/config中。以后直接push和fetch就可以了
10. 之后进行git的相关操作，完成与github的上传与下载操作
11. 命令有`git clone` , `git add filename` , `git add *` , `git commit -m "代码提交信息"` , `git push remote_name master(分支名称)` , `git pull（拉取更新本地的仓库）` , `git merge(自动合并分支，并非每次都能成功，如果不成功，需要手动合并)`,  `git diff`,  `git tag（添加标签，为了每一次合并的版本）`

