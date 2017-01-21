# keynote
重要的知识点
上传到github上的流程：
首先cd到当前目录
$ git init    //初始化

$ touch README

$ git add README   //更新README文件

$ git commit -m 'first commit'//提交更新，并注释信息“first commit”

$ git remote add origin git@github.com:defnngj/hello-world.git   //连接远程github项目   git@github.com:defnngj/hello-world.git这是ssh Keys
$ git push -u origin master   //将本地项目更新到github项目上去



（1）注意：如果出现fatal: remote origin already exists.这种错误，首先要git remote rm origin，然后再执行git remote add origin git@github.com:defnngj/hello-world.git ，就不会报错了




（2）若出现$ git push -u origin master

To git@github.com:yangchao0718/cocos2d.git

 ! [rejected]        master -> master (non-fast-forward)

error: failed to push some refs to 'git@github.com:yangchao0718/cocos2d.git

hint: Updates were rejected because the tip of your current branch is behin

hint: its remote counterpart. Integrate the remote changes (e.g.

hint: 'git pull ...') before pushing again.

hint: See the 'Note about fast-forwards' in 'git push --help' for details.出现这种错误的原因是：github中的README.md文件不在本地代码目录中，需要先执行git pull --rebase origin master，执行上面代码后可以看到本地代码库中多了README.md文件，此时再执行语句 git push -u origin master即可完成代码上传到github。

（3）若出现git commit -m 'first commit'，上面写Untractracked files:
          缺少的文件
          缺少的文件
          缺少的文件
          缺少的文件
此时需要git add 缺少的文件，然后再重新执行。



//定义16进制的颜色
#define UIColorFromHEX(rgbValue) [UIColor \
colorWithRed:((float)((rgbValue & 0xFF0000) >> 16))/255.0 \
green:((float)((rgbValue & 0xFF00) >> 8))/255.0 \
blue:((float)(rgbValue & 0xFF))/255.0 alpha:1.0]
//使用方法：viewColor = UIColorFromHEX(0x22B573);
