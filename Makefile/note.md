# 通配符

## *

*表示匹配所有任何符合条件的。

## ？

？通常在依赖文件列表中使用，匹配所有有更新的目标。

# 函数

## wildcard

用法 ：

```makefile
$(wildcard PATTERN...)
```

其被用作展开为**已经存在的**、**使用空格分开的**、**匹配此模式的**所有文件列表。

例：

```makefile
$(wildcard *.c)
```

用来获取当前文件夹下的所有C文件。

## foreach

用法：

```makefile
$(foreach <var>, <list>, <text>)
```

其将列表<list>中的值依次取出到变量<var>中，将变量<var>进行表达式<text>操作。

例：

```makefile
list := a b c

files := $(foreach n, $(list), $(n).o)
```

files就为 a.o b.o c.o
