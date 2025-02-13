---
title: "示例博文"
subtitle: "示例副标题"
date: 2022-10-07T00:36:54-07:00
draft: false
unlisted: true
series: "示例系列"
seriesNumber: 0
tags: ["示例", "测试"]
description: "展示此博客平台的功能"
coverImage: "https://picsum.photos/id/900/800/600"
autonumbering: true
katex:
  enable: true
  singleDollarDeliminator: false
---

注：此中文版网页由大模型翻译获得

## 示例文本

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Justo nec ultrices dui sapien. Pharetra convallis posuere morbi leo urna molestie at. Elementum nibh tellus molestie nunc non blandit massa. Penatibus et magnis dis parturient montes. Adipiscing commodo elit at imperdiet dui accumsan sit. Venenatis urna cursus eget nunc scelerisque viverra mauris. Vulputate enim nulla aliquet porttitor. Tellus at urna condimentum mattis pellentesque id nibh. Senectus et netus et malesuada fames ac turpis egestas maecenas. Pellentesque adipiscing commodo elit at. Adipiscing commodo elit at imperdiet dui accumsan sit amet nulla. Habitant morbi tristique senectus et netus et. Quam adipiscing vitae proin sagittis nisl. Vel pretium lectus quam id leo in.

Nulla pellentesque dignissim enim sit amet. Nisl rhoncus mattis rhoncus urna neque. Venenatis a condimentum vitae sapien pellentesque habitant. Iaculis eu non diam phasellus vestibulum lorem sed risus ultricies. Lobortis scelerisque fermentum dui faucibus in ornare quam. Dictum non consectetur a erat nam at. Ante in nibh mauris cursus mattis. Volutpat odio facilisis mauris sit. Nec tincidunt praesent semper feugiat nibh sed. Quis blandit turpis cursus in. Quis auctor elit sed vulputate mi. Nunc sed blandit libero volutpat sed cras. Posuere ac ut consequat semper. Lectus quam id leo in vitae turpis massa. Risus nullam eget felis eget. Ac orci phasellus egestas tellus rutrum tellus pellentesque eu tincidunt. Ornare quam viverra orci sagittis eu volutpat odio. Neque gravida in fermentum et sollicitudin ac orci phasellus. Ante metus dictum at tempor commodo ullamcorper a lacus. Commodo nulla facilisi nullam vehicula ipsum a arcu.

Morbi tempus iaculis urna id volutpat. Phasellus vestibulum lorem sed risus ultricies tristique. Fames ac turpis egestas sed tempus urna. Amet aliquam id diam maecenas. Nec ultrices dui sapien eget mi proin sed. Curabitur gravida arcu ac tortor dignissim convallis aenean. In tellus integer feugiat scelerisque varius. Sit amet commodo nulla facilisi nullam vehicula ipsum a arcu. Et egestas quis ipsum suspendisse ultrices gravida dictum. Nec nam aliquam sem et tortor. Amet risus nullam eget felis eget nunc lobortis mattis aliquam. Venenatis urna cursus eget nunc scelerisque viverra mauris. Interdum posuere lorem ipsum dolor sit amet. Faucibus vitae aliquet nec ullamcorper sit amet. Et ultrices neque ornare aenean euismod elementum nisi quis eleifend. Ullamcorper sit amet risus nullam eget felis eget nunc lobortis. Fringilla urna porttitor rhoncus dolor purus non enim.


## 示例图片

```md
![示例图片说明](https://picsum.photos/id/900/800/600 "示例图片标题")
```

![示例图片说明](https://picsum.photos/id/900/800/600 "示例图片标题")

这里还支持无声自动播放的mp4、webm和ogg视频：

```md
![](globe.mp4 "示例视频标题")
```

![](globe.mp4 "示例视频标题")

## 示例YouTube嵌入

YouTube视频可以通过"{{\< youtube video_id \>}}"嵌入：

{{< youtube LXb3EKWsInQ >}}

## 示例\\(\LaTeX\\)

所有\\(\LaTeX\\)公式都可以被选择并以原始"$\LaTeX$"形式复制。选择公式的任何部分或点击公式将会选中所有原始文本，从而可以以原始形式复制。

LaTeX可以以两种格式存在：

- 块级公式
- 行内公式

块级公式：

```md
\\[e = m c^2\\]
```

\\[e = m c^2\\]

或者

```md
$$e = m c^2$$
```

$$e = m c^2$$

行内公式`\\( e^{\pi i} + 1 = 0 \\)`：\\( e^{\pi i} + 1 = 0 \\)。

由于"$"是一个常用字符，除非在前置配置中指定，否则页面不会将`$e^{\pi i} + 1 = 0$`识别为LaTeX。

## 示例代码

你可以使用`行内`代码或代码块（支持行高亮和语法高亮）：

````md
```py {hl_lines=[2], linenos=inline}
def hello_world():
    print("hello world")
```
````

```py {hl_lines=[2], linenos=inline}
def hello_world():
    print("hello world")
```

## 示例表格

表格支持对齐：

```md
| 表头1      |    表头2     |      表头3    |
| :---       |    :----:    |         ---:  |
| (1, 1)     |    (1, 2)    |       (1, 3)  |
| (2, 1)     |    (2, 2)    |       (2, 3)  |
```

| 表头1      |    表头2     |      表头3    |
| :---       |    :----:    |         ---:  |
| (1, 1)     |    (1, 2)    |       (1, 3)  |
| (2, 1)     |    (2, 2)    |       (2, 3)  |

## 示例章节层级 (h2)
### h3
#### h4
##### h5
###### h6

## 其他功能

### 脚注

```md
一些文本[^1]。

[^1]: 这是一个脚注
```

一些文本[^1]。

[^1]: 这是一个脚注

### 水平线

```md
---
```

---

### 引用块

```md
> 一些引用
> > 缩进引用
```

> 一些引用
> > 缩进引用

### 文本格式

```md
*斜体*, **粗体**, 或者 ***粗斜体***。你也可以给文本加入 ~~删除线~~ 。
```

*斜体*, **粗体**, 或者 ***粗斜体***。你也可以给文本加入 ~~删除线~~ 。

### 任务列表

```md
- [ ] 未完成项目
- [x] 已完成项目
```

- [ ] 未完成项目
- [x] 已完成项目

### 链接

```md
<https://example.com>
```

<https://example.com>

```md
<contact@example.com>
```

<contact@example.com>

```md
[示例命名链接](https://example.com)
```

[示例命名链接](https://example.com)

```md
[示例章节链接](#示例-latex)
```

[示例章节链接](#示例-latex)

### 表情符号

表情符号可以通过`:emoji_name:`来渲染。:smile: