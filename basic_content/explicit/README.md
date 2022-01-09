# explicit(显式)关键字那些事

## 读者笔记

为什么要防止隐式类型转换

http://suntus.github.io/2014/10/02/c-explicit%E5%85%B3%E9%94%AE%E5%AD%97/

- explicit 修饰构造函数时，可以防止隐式转换和复制初始化
- explicit 修饰转换函数时，可以防止隐式转换，但按语境转换除外


代码参见:[.explicit.cpp](./explicit.cpp)

参考链接：
> https://stackoverflow.com/questions/4600295/what-is-the-meaning-of-operator-bool-const
