# AsciidocTool
AsciiDoc 工具的使用


## 安装

安装工具 `asciidoc` 和 `fop`, [官方文档](http://www.methods.co.nz/asciidoc/INSTALL.html)

```sh
# macos
brew install asciidoc fop

# linux
apt-get install asciidoc fop 
# 或者
yum install asciidoc fop
```

## 语法

[官方文档](https://powerman.name/doc/asciidoc)

### 头部

Main Header
======
Optional Author Name <optional@author.email>
Optional version, optional date
:Author:    AlternativeWayToSetOptional Author Name
:Email:     <AlternativeWayToSetOptional@author.email>
:Date:      AlternativeWayToSetOptional date
:Revision:  AlternativeWayToSetOptional version

## 渲染输出

### 输出 HTML

```sh
asciidoc -o dist/asciidoc.html docs/asciidoc.txt
```

### 输出 XHTML 

```sh
a2x --format=xhtml -D dist/ docs/asciidoc.txt
```

## 输出 PDF

```sh
# LaTeX 生产者
a2x --format=pdf -D dist/ docs/asciidoc.txt

# FOP 生产者
a2x --fop --format=pdf -D dist/ docs/asciidoc.txt
```

## 定制输出样式

### HTML

```sh
asciidoc -a stylesheet=assets/custom.css -o dist/asciidoc.html asciidoc
```

### PDF

较为复杂

```sh

```
