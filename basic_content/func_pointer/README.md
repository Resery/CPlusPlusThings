# 读者笔记

函数指针的使用场景：

函数指针存在的意义就是可以让你在不同的场景下使用不同的函数来处理相同的数据。

比如说现有一个 buffer 里面存储了一些数据，但是你对这段数据的操作会随需求产生变化。于是你为了应对需求改变而带来的变化，你就需要反复的写一个模子（for 循环，因为处理 buffer 基本就用 for 循环）

然后修改模子里面的代码，当需求特别多的时候你就需要重复写好多相同的模子，浪费代码量而且累。于是就产生除了一种应对方法（不是最终解决方法），在一个 for 循环内我设置一个 flag 检测，也就是检测我

目前到底需要使用哪个操作，然后调用这个操作对应的函数，这个方法确实提升了代码复用率，但是依然很低效因为我还是需要记录所有的 flag 的含义而且每多一个需求我就要多设置一个 flag。

函数指针就是为了解决这种场景下产生的问题。对应的具体操作就是我们可以在 for 循环里面添加一个函数指针，函数指针指向的函数由函数参数指定，然后就 OK 了。每次在调用包含这个 for 循环的函数时把

函数指针传递进来就可以了，也不用 flag 来记录了，也不用写多个模子了，很大的程度上提高了代码复用率。而且也提升了可读性，看到这个指针就知道这个 for 循环是在做什么，而不必去真的阅读了代码之后

才知道这个 for 循环的功能。
