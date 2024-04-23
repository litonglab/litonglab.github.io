# litonglab.github.io

这是LitongLab主页的网站**运行**代码仓库。

# 操作步骤

1. Clone 本项目**配置**代码到本地
```markdown
git clone git@github.com:litonglab/Homepage-configuration-file.git
cd Homepage-configuration-file
```

2. 按需要修改md文件，修改完后保存

3. 使用命令 `hugo server` 可以在本地预览网站，使用命令 `hugo` 可以将网站生成在 public 文件夹下

4. 将修改同步到github代码仓库
```markdown
git add .
git commit -m "请输入你的修改说明"
git push
```

5. 退出Homepage-configuration-file文件夹，Clone 本项目**运行**代码到本地
```markdown
cd ..
git clone git@github.com:litonglab/litonglab.github.io.git
```

6. 重新进入Homepage-configuration-file文件夹，将public 文件夹下的所有文件和文件夹拷贝到litonglab.github.io文件夹下，同名的文件和文件夹请选择覆盖

7. 退出Homepage-configuration-file文件夹，进入litonglab.github.io.git文件夹，将代码同步到github
```markdown
cd ..
cd litonglab.github.io.git
git add .
git commit -m "请输入你的修改说明"
git push
```
8. 大功告成！注意仔细预览一下，double check一下修改是否生效，有没有格式问题，有没有低级错误……
