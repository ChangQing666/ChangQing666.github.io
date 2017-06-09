---
title: HEXO本地博客搭建步骤
---

## HEXO本地博客搭建步骤
- 0.准备工作
   
   > 1. 安装`node`
   > 2. 安装`git`
   > 3. 创建仓库`username.github.io`
   > 4. 克隆仓库到本地
- 1.安装hexo脚手架

    ```
        cnpm install hexo-cli -g
    ```
- 2.hexo 初始化blog博客目录

    ```
        hexo init blog
    ```
- 3.进入blog目录
    
   ```
       cd blog
   ```
- 4.安装插件
    
    ```
        cnpm install
    ```

- 5.写完markdown文件后，发布文章

    ```
        hexo generate
    ```
- 6.浏览器预览

    ```
     hexo server
    （如果报错需要安装hexo-server插件： npm install hexo-server --save）
    ```


- 7.将本地博客与github关联（修改_config.yml中的deploy参数如下）`注意：type值为git并不是github`
    ```
     deploy:
          type: git
          repository: https://github.com/ChangQing666/ChangQing666.github.io.git
          branch: master
    ```
- 8.将本地发送至github上
    ```
        hexo deploy  (如果报错需要安装  npm install hexo-deployer-git )
    ```



### 从github上面拉下代码进行修改提交的步骤：

---

- 1.克隆
  ```
        git clone https://github.com/ChangQing666/ChangQing666.github.io.git
    ```
- 2.进入ChangQing666.github.io文件夹
    ```
        cd ChangQing666.github.io
    ```
- 3.检查状态

    ```
        git status
    ```
- 4.查看分支
  
    ```
         git branch
    ```
- 5.查看本地和远程分支
    ```
        git branch -a
    ```
- 6.安装nodule_moudles(如果有nodule_moudles,就删除node_modules文件夹，并重新安装)
    ```
        cnpm install
        或
    rm -rf node_modules/ && npm install
    ```

- 7.查看hexo版本

    ```
     hexo -v
    ```
- 8.生成html

    ```
     hexo generate
    ```
- 9.发布到gitHub
    
    ```
    hexo deploy
    ```

