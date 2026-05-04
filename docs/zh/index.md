---
icon: lucide/rocket
---

# 快速开始

完整文档请访问 [zensical.org](https://zensical.org/docs/)。

## 命令

* [`zensical new`][new] - 创建一个新项目
* [`zensical serve`][serve] - 启动本地 Web 服务器
* [`zensical build`][build] - 构建你的站点

  [new]: https://zensical.org/docs/usage/new/
  [serve]: https://zensical.org/docs/usage/preview/
  [build]: https://zensical.org/docs/usage/build/

## 示例

### 提示块（Admonitions）

> 查看[文档](https://zensical.org/docs/authoring/admonitions/)

!!! note

    这是一个**提示（note）**块。可用于提供有帮助的信息。

!!! warning

    这是一个**警告（warning）**块。请注意！

### 折叠详情（Details）

> 查看[文档](https://zensical.org/docs/authoring/admonitions/#collapsible-blocks)

??? info "点击展开查看更多信息"

    这部分内容会在点击展开后显示。
    非常适合 FAQ 或较长说明。

## 代码块

> 查看[文档](https://zensical.org/docs/authoring/code-blocks/)

``` python hl_lines="2" title="代码块"
def greet(name):
    print(f"你好，{name}！") # (1)!

greet("Python")
```

1.  > 查看[文档](https://zensical.org/docs/authoring/code-blocks/#code-annotations)

    代码注解可以为代码行附加说明。

也可以进行行内高亮：`#!python print("你好，Python！")`。

## 内容标签页（Tabs）

> 查看[文档](https://zensical.org/docs/authoring/content-tabs/)

=== "Python"

    ``` python
    print("来自 Python 的问候！")
    ```

=== "Rust"

    ``` rs
    println!("来自 Rust 的问候！");
    ```

## 图表

> 查看[文档](https://zensical.org/docs/authoring/diagrams/)

``` mermaid
graph LR
  A[开始] --> B{有错误吗？};
  B -->|是| C[嗯……];
  C --> D[调试];
  D --> B;
  B ---->|否| E[成功！];
```

## 脚注

> 查看[文档](https://zensical.org/docs/authoring/footnotes/)

这是一句带脚注的句子。[^1]

将鼠标悬停其上可查看提示。

[^1]: 这是脚注内容。


## 格式化

> 查看[文档](https://zensical.org/docs/authoring/formatting/)

- ==这是高亮标记==
- ^^这是下划线（插入）^^
- ~~这是删除线（删除）~~
- H~2~O
- A^T^A
- ++ctrl+alt+del++

## 图标与表情（Emojis）

> 查看[文档](https://zensical.org/docs/authoring/icons-emojis/)

* :sparkles: `:sparkles:`
* :rocket: `:rocket:`
* :tada: `:tada:`
* :memo: `:memo:`
* :eyes: `:eyes:`

## 数学公式

> 查看[文档](https://zensical.org/docs/authoring/math/)

$$
\cos x=\sum_{k=0}^{\infty}\frac{(-1)^k}{(2k)!}x^{2k}
$$

!!! warning "需要额外配置"
    请注意，本页通过 `script` 标签引入了 MathJax，而默认生成配置中并未开启，
    以避免在不需要公式的页面中也加载它。若你的页面比这个入门示例更依赖数学公式，
    请参考文档了解如何为所有页面统一配置。

<script id="MathJax-script" src="https://unpkg.com/mathjax@3/es5/tex-mml-chtml.js"></script>
<script>
  window.MathJax = {
    tex: {
      inlineMath: [["\\(", "\\)"]],
      displayMath: [["\\[", "\\]"]],
      processEscapes: true,
      processEnvironments: true
    },
    options: {
      ignoreHtmlClass: ".*|",
      processHtmlClass: "arithmatex"
    }
  };

  document$.subscribe(() => {
    MathJax.startup.output.clearCache()
    MathJax.typesetClear()
    MathJax.texReset()
    MathJax.typesetPromise()
  })
</script>

## 任务列表

> 查看[文档](https://zensical.org/docs/authoring/lists/#using-task-lists)

* [x] 安装 Zensical
* [x] 配置 `zensical.toml`
* [x] 编写出色的文档
* [ ] 部署到任意平台

## 悬浮提示（Tooltips）

> 查看[文档](https://zensical.org/docs/authoring/tooltips/)

[悬停查看提示][example]

  [example]: https://example.com "我是一个提示框！"
