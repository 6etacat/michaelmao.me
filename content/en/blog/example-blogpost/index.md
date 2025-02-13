---
title: "Example Blogpost"
subtitle: "Example Subtitle"
date: 2022-10-07T00:36:54-07:00
draft: false
unlisted: true
series: "Example Series"
seriesNumber: 0
tags: ["example", "test"]
description: "Showcase of the capabilities of this blogging platform"
coverImage: "https://picsum.photos/id/900/800/600"
autonumbering: true
katex:
  enable: true
  singleDollarDeliminator: false
---

## Example Text

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Justo nec ultrices dui sapien. Pharetra convallis posuere morbi leo urna molestie at. Elementum nibh tellus molestie nunc non blandit massa. Penatibus et magnis dis parturient montes. Adipiscing commodo elit at imperdiet dui accumsan sit. Venenatis urna cursus eget nunc scelerisque viverra mauris. Vulputate enim nulla aliquet porttitor. Tellus at urna condimentum mattis pellentesque id nibh. Senectus et netus et malesuada fames ac turpis egestas maecenas. Pellentesque adipiscing commodo elit at. Adipiscing commodo elit at imperdiet dui accumsan sit amet nulla. Habitant morbi tristique senectus et netus et. Quam adipiscing vitae proin sagittis nisl. Vel pretium lectus quam id leo in.

Nulla pellentesque dignissim enim sit amet. Nisl rhoncus mattis rhoncus urna neque. Venenatis a condimentum vitae sapien pellentesque habitant. Iaculis eu non diam phasellus vestibulum lorem sed risus ultricies. Lobortis scelerisque fermentum dui faucibus in ornare quam. Dictum non consectetur a erat nam at. Ante in nibh mauris cursus mattis. Volutpat odio facilisis mauris sit. Nec tincidunt praesent semper feugiat nibh sed. Quis blandit turpis cursus in. Quis auctor elit sed vulputate mi. Nunc sed blandit libero volutpat sed cras. Posuere ac ut consequat semper. Lectus quam id leo in vitae turpis massa. Risus nullam eget felis eget. Ac orci phasellus egestas tellus rutrum tellus pellentesque eu tincidunt. Ornare quam viverra orci sagittis eu volutpat odio. Neque gravida in fermentum et sollicitudin ac orci phasellus. Ante metus dictum at tempor commodo ullamcorper a lacus. Commodo nulla facilisi nullam vehicula ipsum a arcu.

Morbi tempus iaculis urna id volutpat. Phasellus vestibulum lorem sed risus ultricies tristique. Fames ac turpis egestas sed tempus urna. Amet aliquam id diam maecenas. Nec ultrices dui sapien eget mi proin sed. Curabitur gravida arcu ac tortor dignissim convallis aenean. In tellus integer feugiat scelerisque varius. Sit amet commodo nulla facilisi nullam vehicula ipsum a arcu. Et egestas quis ipsum suspendisse ultrices gravida dictum. Nec nam aliquam sem et tortor. Amet risus nullam eget felis eget nunc lobortis mattis aliquam. Venenatis urna cursus eget nunc scelerisque viverra mauris. Interdum posuere lorem ipsum dolor sit amet. Faucibus vitae aliquet nec ullamcorper sit amet. Et ultrices neque ornare aenean euismod elementum nisi quis eleifend. Ullamcorper sit amet risus nullam eget felis eget nunc lobortis. Fringilla urna porttitor rhoncus dolor purus non enim.

## Example Image

```md
![example image alt](https://picsum.photos/id/900/800/600 "example image title")
```

![example image alt](https://picsum.photos/id/900/800/600 "example image title")

This also supports silent autoplay mp4, webm, and ogg videos for small-sized animated images:

```md
![](globe.mp4 "example video title")
```

![](globe.mp4 "example video title")

## Example YouTube Embed

YouTube videos can be embedded with "{{\< youtube video_id \>}}":

{{< youtube LXb3EKWsInQ >}}

## Example \\(\LaTeX\\)

All \\(\LaTeX\\) equations can be selected and copied as its raw "$\LaTeX$" form. Selecting any part of the \\(\LaTeX\\) equation or clicking on the equation will cause all the raw text be selected, and can thus be copied in its raw form. 

Latex can exist in two formats: 

- block equation
- inline equation

A block equation:

```md
\\[e = m c^2\\]
```

\\[e = m c^2\\]

or

```md
$$e = m c^2$$
```

$$e = m c^2$$

An inline equation `\\( e^{\pi i} + 1 = 0 \\)`: \\( e^{\pi i} + 1 = 0 \\). 

Since "$" is a commonly used character, the page does not recognize `$e^{\pi i} + 1 = 0$` as LaTeX unless specified in the front matter.

## Example Code

You can use `inline` code or code blocks (with line highlighting and syntax highlighting):
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

## Example Table

Tables work with alignment:

```md
| Header 1    |   Header 2   |     Header 3  |
| :---        |    :----:    |          ---: |
| (1, 1)      |    (1, 2)    |        (1, 3) |
| (2, 1)      |    (2, 2)    |        (2, 3) |
```

| Header 1    |   Header 2   |     Header 3  |
| :---        |    :----:    |          ---: |
| (1, 1)      |    (1, 2)    |        (1, 3) |
| (2, 1)      |    (2, 2)    |        (2, 3) |

## Example Section Hierarchy (h2)
### h3
#### h4
##### h5
###### h6

## Other Random Stuff

### Footnotes

```md
Some text[^1].

[^1]: This is a footnote
```

Some text[^1].

[^1]: This is a footnote

### Horizontal Line

```md
---
```

---

### Block Quote

```md
> Some quote
> > Indented quote
```

> Some quote
> > Indented quote

### Text Formatting

```md
*Italicized*, **bolded**, or ***both***. You can also ~~strikethrough~~ text. 
```

*Italicized*, **bolded**, or ***both***. You can also ~~strikethrough~~ text. 

### Task List

```md
- [ ] Unfinished item
- [x] Item done
```

- [ ] Unfinished item
- [x] Item done

### Links

```md
<https://example.com>
```

<https://example.com>

```md
<contact@example.com>
```

<contact@example.com>

```md
[example named link](https://example.com)
```

[example named link](https://example.com)

```md
[example link to sections](#example-latex)
```

[example link to sections](#example-latex)

### Emoji

Emojis can be rendered with `:emoji_name:`. :smile:

### GitHub Gist

GitHub Gists can be embedded with "{{\< gist username gist_id \>}}":

{{< gist michaelmyc a4e02a04cbb3e526d029bb0f21e1f959 >}}