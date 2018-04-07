:hotel:[Return to JAVA Home Page](https://github.com/geophydog/Java)

***

```
Exception in thread "main" java.lang.NoSuchMethodError
```
_原因:_
```
(1) 第一个常见原因jar包中确实没有这个方法，所以虚拟机根本没有加载这个方法。

(2) 第二个常见原因是jar包冲突了。导致虚拟机不知道加载哪一个，所以就导致了加载失败，从而找不到这个方法。

(3) 第三个，也许就是包含在第二种情况中，该方法只有抽象定义，而没有具体实现。我今天的遇到的是第二种吧。
```
