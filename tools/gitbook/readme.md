# GitBook 

## 概述

GitBook 是使用 GitHub / Git 和 Markdown（或AsciiDoc）构建漂亮书籍的命令行工具（和Node.js库）。
GitBook 可以将您的内容作为网站（可定制和可扩展）或电子书（PDF，ePub或Mobi）输出。
GitBook.com 是使用 GitBook 格式创建和托管图书的在线平台。它提供托管，协作功能和易于使用的编辑器。

## 目录结构

GitBook使用简单的目录结构。在 SUMMARY （即 SUMMARY.md 文件）中列出的所有 Markdown / Asciidoc 文件将被转换为 HTML。多语言书籍结构略有不同。

一个基本的 GitBook 电子书结构通常如下：

```
.
├── book.json
├── README.md
├── SUMMARY.md
├── chapter-1/
|   ├── README.md
|   └── something.md
└── chapter-2/
    ├── README.md
    └── something.md
```

## 项目与子目录集成

对于软件项目，您可以使用子目录（如 docs/ ）来存储项目文档的图书。您可以配置根选项来指示 GitBook 可以找到该图书文件的文件夹：

```
.
├── book.json
└── docs/
    ├── README.md
    └── SUMMARY.md
```

## Summary

GitBook 使用 SUMMARY.md 文件来定义本书的章节和子章节的结构。 SUMMARY.md 文件用于生成本书的目录。

SUMMARY.md 的格式是一个链接列表。链接的标题将作为章节的标题，链接的目标是该章节文件的路径。

向父章节添加嵌套列表将创建子章节。

### 简单示例：

```
# Summary
 
* [Part I](part1/README.md)
    * [Writing is nice](part1/writing.md)
    * [GitBook is nice](part1/gitbook.md)
* [Part II](part2/README.md)
    * [We love feedback](part2/feedback_please.md)
    * [Better tools for authors](part2/better_tools.md)

```

每章都有一个专用页面（part#/README.md），并分为子章节。

### 锚点

目录中的章节可以使用锚点指向文件的特定部分。

```
# Summary
 
### Part I
 
* [Part I](part1/README.md)
    * [Writing is nice](part1/README.md#writing)
    * [GitBook is nice](part1/README.md#gitbook)
* [Part II](part2/README.md)
    * [We love feedback](part2/README.md#feedback)
    * [Better tools for authors](part2/README.md#tools)

```

### 部分

目录可以分为以标题或水平线 ---- 分隔的部分：
```
# Summary
 
### Part I
 
* [Writing is nice](part1/writing.md)
* [GitBook is nice](part1/gitbook.md)
 
### Part II
 
* [We love feedback](part2/feedback_please.md)
* [Better tools for authors](part2/better_tools.md)
 
----
 
* [Last part without title](part3/title.md)
```

Parts 只是章节组，没有专用页面，但根据主题，它将在导航中显示。

## Glossary

允许您指定要显示为注释的术语及其各自的定义。根据这些术语，GitBook 将自动构建索引并突出显示这些术语。

GLOSSARY.md 的格式是 h2 标题的列表，以及描述段落：

```
## Term
Definition for this term
 
## Another term
With it's definition, this can contain bold text
and all other kinds of inline markup ...
```