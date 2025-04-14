# Homepage-configuration-file

这是LitongLab主页的网站**配置**代码仓库。

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

# 附：Hugo 网站使用手册

Hugo 是一个静态网站生成器，它将您的内容组织为静态网页并生成网站。

以下是 hugo 中常用文件夹的作用：

- `content`：存放您的所有内容的文件夹。您可以在这里创建文件夹来组织您的内容，例如 `content/blog` 和 `content/docs`。

- `layouts`: 存放网站布局的文件夹。布局是用来定义内容呈现方式的文件，可以使用 Go 模板。

- `static`: 存放静态资源，如图片，CSS 和 JavaScript 文件。

- `themes`: 存放主题文件。hugo 允许您使用预先定义好的主题来更改网站的外观和布局。

- `config.toml`: 这是网站配置文件，用来配置网站元数据，如标题，描述和主题。

在您的网站中使用 hugo，您需要创建和组织内容，并使用布局和主题来呈现内容。您还可以使用配置文件来配置网站元数据。

使用命令 `hugo server` 可以在本地预览网站, 使用命令 `hugo` 可以将网站生成在 public 文件夹下，使用静态托管服务将 public 文件夹放到服务器即可发布网站。

这只是一个简单的使用说明，详情请查看[hugo](https://gohugo.io/documentation/)的官方文档以及主题[hugo-theme-monochrome](https://kaiiiz.github.io/hugo-theme-monochrome/)的官方网站。

## Content

`content`文件夹存放您的所有内容，它包括一些页面和文章。

- 每个文件夹都可以包含一个或多个页面或文章。文件夹结构可以用来组织内容，例如将博客文章分类为不同的主题。
- 每个页面或文章都应该用一个单独的文件表示，并使用一种结构化格式存储，如Markdown或HTML。
- 文件中可以使用front matter来定义元数据，如标题，描述和标签。 元数据可以被用来在网站中导航和搜索。

举个例子，在 `content/blog/` 创建一个 "my-first-post.md" 的文件，里面的内容可以是这样的:

```markdown
---
title: "My First Blog Post"
date: 2020-01-01
tags: ["hugo", "blogging"]
---

This is the content of my first blog post.
```

这样就完成了一篇博客文章的创建，在hugo 中通过对应的模板来呈现文章的内容,通过 front matter 的标签,日期来呈现文章的分类, 标题,等信息。
请记住，您可以根据您的需要自由组织内容和使用元数据。这只是一个示例，您可以根据自己的需要来自定义文件结构和呈现。

## Static 

`static`文件夹用来存储静态资源，如图片、CSS 和 JavaScript 文件。

- 你可以在这个文件夹中建立子文件夹来组织文件，例如: `static/css/`,`static/js/`,`static/img/`
- 这些文件可以在网站中使用相对路径进行引用，例如: `/css/styles.css`。
- 所有文件夹中的文件都将被复制到最终生成的网站的 `public` 文件夹中,并且将与你配置的文件结构保持一致
- 文件夹中的文件可以在网站中使用相对路径引用，如`/img/example.jpg`

这样在你的网页中可以使用相对路径来引用这些静态文件,如图片和 CSS 样式等。
请注意，如果您使用的是主题，则应该查看主题的文档以了解如何使用静态资源。

## config.toml

`config.toml`文件是hugo的主配置文件，它存储了有关网站的元数据，如标题、作者、链接和语言等。

- 你可以在config.toml中设置主题，页面排序方式，内容类型，菜单，小工具，以及其他结构性和布局性配置项目。
- 可以通过导入配置文件来实现多语言配置
- 你还可以添加自定义变量和设置,以便在您的网站中使用.

举个例子,在 config.toml 文件中你可以设置如下配置项来更改你网站的标题，首页显示的内容，

```toml
baseURL = "https://example.com"
title = "My Website"
languageCode = "en-us"
paginate = 10
enableEmoji = true

[params]
  subtitle = "A place for my thoughts"
  show_comments = false
```

## 杂项

1.图片的插入:

```markdown
{{< figure src=""(填入相对地址) caption=""(图片下的描述文字) >}}
```

2.一些小图标：

```markdown
{{< icon name="github"      link="https://github.com/kaiiiz/hugo-theme-monochrome" >}}
{{< icon name="facebook"    link="https://github.com/kaiiiz/hugo-theme-monochrome" >}}
{{< icon name="rss"         link="https://github.com/kaiiiz/hugo-theme-monochrome" >}}
{{< icon name="twitter"     link="https://github.com/kaiiiz/hugo-theme-monochrome" >}}
{{< icon name="mail"     link="https://github.com/kaiiiz/hugo-theme-monochrome" >}}
```

3.公式的使用：

首先需要在content/..md文件的头选项中插入 

```markdown
math: true
```

然后可以正常书写数学公式：
$\sqrt{3x-1}+(1+x)^2$ <!--使用单个$表示左对齐，两个$表示居中。-->

4.面包屑

```markdown
{{< breadcrumbs >}}
```

效果如下：
{{< breadcrumbs >}}

5.颜色块的使用

如下代码效果为：

```markdown
hello world
{{< /color-block >}}
```

hello world
{{< /color-block >}}

6.启用表情符号。

该[emojify](https://gohugo.io/functions/emojify/)函数可以直接在模板或[内联短代码](https://gohugo.io/templates/shortcode-templates/#inline-shortcodes)中调用。

要全局启用表情符号，请在您的站点配置enableEmoji中设置为true，然后您可以直接在configuration文件中键入表情符号速记代码；
例如

```markdown
:exclamation:
```

代表了:exclamation:

[表情符号备忘单](http://www.emoji-cheat-sheet.com/)是表情符号速记代码的有用参考。

注意:以上步骤在 Hugo 中启用了 Unicode 标准表情符号字符和序列，但是这些字形的呈现取决于浏览器和平台。要设置表情符号的样式，您可以使用第三方表情符号字体或字体堆栈；例如

```markdown
.emoji {
  font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
}
```