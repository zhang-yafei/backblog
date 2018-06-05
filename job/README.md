##新环境环境搭建流程
1. npm install -g hexo
2. hexo init

###常规命令
* hexo new "postName" //新建文章
* hexo new page "pageName" //#新建页面
* hexo server  //本地开发环境调试
* hexo clean   //清理静态文件
* hexo generate  //重新生成静态文件
* hexo deploy   //部署到服务器




##错误集锦
1. 当hexo deploy时，发生"in unpopulated submodule 'job/.deploy_git'"错误时，删除目录'.deploy_git'
	```hexo g
    hexo d
    ```
即可正常使用