# aliyunTest
阿里云服务器测试Git总结<br>
====
原料
----
* 阿里云服务器
* github账户
* Xshell
#####
步骤
----
* 1.在本机(w7)利用Xshell创建会话登录阿里云服务器
* 2.创建目录下载git
  * 命令：sudo apt-get install git
  * 注意：执行上述命令后可能会出现 Unable to locate package 错误
  * 解决方案：因为新装的ubuntu系统,没有update的原因,输入命令：sudo apt-get update ,之后继续执行安装命令即可。
* 3.git基本配置
  * 3.1 创建git仓库目录
    * mkdir git
    * cd git
  * 3.2 初始化git
    * git init
  * 3.3 写入测试文件
    * 覆盖型写法
    * echo "xxxx" > x.txt
    * 添加型写法
    * echo "xxxx" >> x.txt
  * 3.4 提交文件到缓存区
    * git add x.txt
  * 3.5 提交文件到HEAD
    * git commit -m x.txt
    * 这里会出现提交异常，需要填写个人信息，解决方案：
    * git config --global user.name "xxx"
    * git config --global user.email "xxx"
    * 填写完整后即可。
 * 4.在阿里云上生成公匙
    * ssh-keygen -C "你的github账号" -f ~/.ssh/github
    * 查看方法
    * cd ..  //进入根目录(/root)
    * cd .ssh
    * ls
    * 即可看到github.pub文件
 * 5.进入个人账户进行设置SSH Key
    * 这里介绍下怎样打开github.pub文件，获取公匙
    * vi github.pub //打开文件
    * 复制SSH key 即可
 * 6.创建一个新仓库repository
    * 创建后进入仓库复制https地址，执行以下命令
    * git remote add origin https://github.com/Encounter77/text.git //增加到remote
    * git push origin master  //push到github上
    * 输入用户名及密码即可。
 ######
 第一次写贴<br>
 :relaxed:
 :relaxed:
