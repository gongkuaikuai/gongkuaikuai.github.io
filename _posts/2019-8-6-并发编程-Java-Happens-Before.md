**用Happens-Before对vilotile对语义进行增强**

###### Happens-Before定义
- 前面一个操作对后续操作是可见的。
- 虽然远隔千里，但一个人所想，能被另一个人所感知。
- **Happens-Before约束了编译器但优化行为，虽允许编译器优化，但是要求编译器优化后一定遵守Happens-Before规则。**

###### Happens-Before规则
1. 程序但顺序性规则
1. volatile变量规则。对一个volatile变量的写操作，Happens-Before于后续对这个volatile变量的读操作。
1. 传递性。如果A Happens-Before B，且B Happens-Before C，那么A Happens-Before C。
1. 官称中的所规则。对一个锁的解锁Happens—Before于后续对这个锁对加锁。
1. 线程start（）规则。主线程A启动子线程B后，子线程B能够看到主线程在启动子线程B前对操作。
1. 线程join() 规则。主线程A等待子线程B完成（主线程A通过调用子线程B对join() 方法实现），当子线程B完成后，主线程能看到子线程的操作。

**觉得Happens-Before都是些废话。考察它是对有序性做的一个修补，需要了解有序性**
