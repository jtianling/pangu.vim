
# PanGu.vim

美式盘古插件用于自动格式化、标准化中文排版。同时改进了一些对程序员更友好的规则, 比如所有标点符号都使用英文, 所以理论上可以对任何代码(包括盘古不推荐的HTML等)无害开启. (起码目标是这样)  

它会将一些非标准，或不推荐的排版方式，在保存文件时进行自动格式化、标准化。

## 功能

* 中英文字符间增加一个半角空白。
* 中文前后的半角标点转成全角标点。 -> 全角标点转成半角标点, 中文标点转成英文标点
* 全角英文、数字转成半角字符。
* 感叹号、问号最多允许连续重复 3 次。(不开启)
* 其他中文标点符号不允许重复出现。(不开启)

## 支持的文件格式

推荐在以下文件格式中使用：

* Markdown (*.md, *.markdown)
* Text (*.text, *.txt)
* Wiki (*.wiki)
* Vim 中文文档 (*.cnx)

如果想在其他格式的文件中使用这个功能，可以执行 `:Pangu` 命令。

同时可以在 vimrc 中开启自动规范化功能。开启方式：

```viml
autocmd BufWritePre *.markdown,*.md,*.text,*.txt,*.wiki,*.cnx call PanGuSpacing()
```

> **注意：目前只对纯文本格式的文件支持较好，其他如 html 等，请谨慎开启。**
>
> 如果有合适的文件格式推荐，请提交 [Issue](https://github.com/hotoo/pangu.vim/issues)

## 安装

via Vundle:

```
Bundle "hotoo/pangu.vim"
```

## 用法

### `:Pangu` 命令

手动执行该命令，将当前文件进行规范化。

### `:PanguDisable` 命令

禁止自动规范化。

### `:PanguEnable` 命令

启用自动规范化。

## 参考

* [中文文案排版指北](https://github.com/sparanoid/chinese-copywriting-guidelines)
