### 交互模式
```
python
>>> the_world_is_flat = True
>>> if the_world_is_flat:
...     print("Be careful not to full off!")
...
Be careful not to full off!
```
### 源文件的字符编码
默认情况下，Python 源码文件的编码是 UTF-8。这种编码支持世界上大多数语言的字符，可以用于字符串字面值、变量、函数名及注释 —— 尽管标准库只用常规的 ASCII 字符作为变量名或函数名，可移植代码都应遵守此约定。要正确显示这些字符，编辑器必须能识别 UTF-8 编码，而且必须使用支持文件中所有字符的字体。

如果不使用默认编码，则要声明文件的编码，文件的 第一 行要写成特殊注释。句法如下：
```python
# -*- coding: encoding -*-
```
其中，encoding 可以是 Python 支持的任意一种 codecs。

比如，声明使用 Windows-1252 编码，源码文件要写成：
```python
# -*- coding: cp1252 -*-
```
第一行 的规则也有一种例外情况，源码以 UNIX "shebang" 行 开头。此时，编码声明要写在文件的第二行。例如：
```python
#!/usr/bin/env python3
# -*- coding: cp1252 -*-
```