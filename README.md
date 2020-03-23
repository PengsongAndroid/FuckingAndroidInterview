# FuckingAndroidInterview
Andoird Interview is fucking

[所有知识点脑图查看](https://github.com/PengsongAndroid/FuckingAndroidInterview/blob/master/interview.png)


# 面试

## Android

### 基础知识

#### Activity

##### Dialog、DialogFragment对生命周期影响

##### 透明Activity对生命周期影响

##### LaunchModel对生命周期影响

##### 屏幕旋转生命周期

##### 数据的保存与恢复

##### Intent

###### 可以传输的数据类型，以及传输原理

###### 显示、隐式

###### 不同的Action的作用

##### style

##### ActivityThread工作原理

#### fragment

##### 切换时的生命周期

##### 与activity的通信

##### 数据保存与恢复

#### Context

#### Application

#### Touch事件分发

##### 滑动冲突的解决

##### 主要涉及的方法、ACTION_CANCEL时机

#### Service

##### 启动方式

##### IntentService

##### 与activity通信方式

##### 保活手段

#### BroadcastReceiver

##### 注册方式

##### 数据的限制

##### 原理

##### LocalBroadCastRecevier

##### 销毁方式

#### ContentProvider

#### View

##### View层级

##### 绘制流程

##### 自定义View

###### 重写方法，自定义步骤

###### 自定义View中如何开启硬件加速

##### Animation

###### TweenAnimation

###### FrameAnimation

###### Property Animation

####### ValueAnimator 

####### ObjectAnimatior

###### 对比总结

#### RecycleView

##### 优化

##### 使用的设计模式及优势

##### 头布局、瀑布流实现

#### ConstraintLayout

#### 数据

##### SharePreference

###### 原理

###### 优缺点

##### database

###### 使用场景及步骤

###### 注意事项，更改表结构时需要更新版本

###### 优缺点

###### 常用开源库

#### Handler

##### 原理，引出另外两个重要的类

##### 延迟发送如何实现

##### 如何保证消息的顺序

##### 内存泄漏及解决

##### HandlerThread

##### ThreadLocal

#### AsyncTask粗看一下

#### 各个版本主要特性

#### Xml解析方式及优劣

#### json解析方式

#### 序列化

##### Serializable

##### Parcelable

##### 实现方式及优劣势

#### gradle

##### 常用配置、脚本

##### 渠道包、不同版本包控制

#### HttpClient和HttpConnection的区别

#### webview

##### webview加载优化

##### h5交互

###### addJavascriptInterface与h5互相调用方法

###### 通过shouldOverridUrlLoading拦截处理

###### 读取cookie

###### 通过prompt、console、log、alert重新使用极少

#### 屏幕适配

##### dpi计算

##### 传统方案

###### 权重

###### 多分辨率资源、布局

##### 不同文件夹图片对内存的消耗，drawable、mipmap区别

##### 头条方案

##### 刘海屏、全面屏、曲面屏适配

### 开源库

#### 网络

##### okhttp

###### 架构设计优势

###### 缓存实现

###### 遇到的问题及解决

###### 为何高效，对于网络层的优化

###### 长连接是什么、keep-alive标签意义、连接复用

##### volley

#### 图片加载

##### glide

###### 缓存逻辑

##### fresco

##### 对比总结优缺点

#### 热修复/插件化

##### ClassLoader类型及工作机制

##### 插件化实现原理

##### 热修复实现思路

##### thinker

###### 如何加载patch

###### 如何生成patch

###### 资源文件如何替换

##### andfix

#### Rxjava

##### 基本原理

##### 常用类的概念定义

##### 常用操作符

#### Butterknife

##### 注解分类及原理，apt

##### AOP OOP IOC思维

#### Retrofit

##### 设计构思及优点

#### EventBus

#### 设计模式总结

### 性能优化

#### App启动速度优化

##### 冷启动

##### 热启动

###### sdk延迟初始化

#### 内存泄漏

##### 常见内存泄漏场景

##### 分析工具

#### 内存溢出

##### 常见oom场景及解决手段

##### 软弱引用

##### bitmap

###### 内存计算

###### 常见压缩或优化手段

#### 布局优化

##### 不同layout性能对比

##### viewstub、merge使用方式，可能碰到的问题

##### 分析工具

#### crash优化

##### CrashHandler实现原理

##### 这里肯定会问解决过哪些困难的bug，去网上找一找特定机型的bug

#### 网络、流量优化

##### 网络优化

##### 弱网环境通信方案

##### 缓存请求，合并请求，减少请求次数，减少请求体

#### 内存优化

#### apk体积优化

#### 电量优化

#### 性能分析工具

#### crash应急处理

### 架构设计

#### mvp

#### mvvm

#### 谷歌官方组件Lifecycle

#### 组件化设计及常见问题解决（路由、资源、依赖关系）

#### 对比优劣及原理

### JNI

#### Java调用C++

#### C++调用java

#### 传输数据类型

#### 注册native方法方式

#### so加载流程及生命周期

### Binder

#### 进程间通讯方式

##### 管道

##### 共享内存

##### socket

##### 信号量

##### 信号

##### 消息队列

##### android采用binder原因及优点

#### 原理

#### aidl

#### 大内存数据如何传输

#### Activity启动流程

#### AMS、PMS、WMS

### Android Framwork

#### Android系统架构

#### Android启动流程

#### APK安装流程

#### Android进程内存分配

### Android安全

#### 加壳原理

#### 脱壳原理

#### 混淆

##### proguard配置

##### stringFog对静态字符串加密

##### andres对资源加密

##### 脚本修改四大组件命名随机打乱目录

##### Obfuscapk修改smali打乱调用关系链

#### 反编译

##### 常用反编译工具及流程

##### smali基础语法

#### 数据安全

##### 网络传输

###### 加密url及body

##### 数据加密存储

#### dex校验

##### 读取安全目录下的dex文件判断hash值是否一致（是否一定能读取到/data/app/xx.apk）

#### 基础手段

##### 防调试

##### 重要逻辑用c++写

##### 设置组件访问权限

#### 常见加密算法举例及其思路

### Apk

#### 签名算法原理及签名过程

#### apk结构

#### Debug跟Release的APK的区别

### 虚拟机

#### JVM

#### Dalvik

#### ART

#### 总结优缺点，垃圾回收机制

### 补充问题

#### SurfaceView

#### Bitmap大图加载

#### 文件断点续传

#### 换肤实现

## Java

### 基础 

#### 关键字final、static修饰方法/变量，原理及适用场景

#### 多态

#### String，StringBuffer，StringBuilder

#### 内部类、静态内部类、匿名内部类

#### 抽象类/接口概念及适用场景

11、抽象类和接口区别？
共同点

是上层的抽象层。
都不能被实例化。
都能包含抽象的方法，这些抽象的方法用于描述类具备的功能，但是不提供具体的实现。
区别：

1、在抽象类中可以写非抽象的方法，从而避免在子类中重复书写他们，这样可以提高代码的复用性，这是抽象类的优势，接口中只能有抽象的方法。
2、多继承：一个类只能继承一个直接父类，这个父类可以是具体的类也可是抽象类，但是一个类可以实现多个接口。
3、抽象类可以有默认的方法实现，接口根本不存在方法的实现。
4、子类使用extends关键字来继承抽象类。如果子类不是抽象类的话，它需要提供抽象类中所有声明方法的实现。子类使用关键字implements来实现接口。它需要提供接口中所有声明方法的实现。
5、构造器：抽象类可以有构造器，接口不能有构造器。
6、和普通Java类的区别：除了你不能实例化抽象类之外，抽象类和普通Java类没有任何区别，接口是完全不同的类型。
7、访问修饰符:抽象方法可以有public、protected和default修饰符，接口方法默认修饰符是public。你不可以使用其它修饰符。
8、main方法:抽象方法可以有main方法并且我们可以运行它接口没有main方法，因此我们不能运行它。
9、速度:抽象类比接口速度要快，接口是稍微有点慢的，因为它需要时间去寻找在类中实现的方法。
10、添加新方法:如果你往抽象类中添加新的方法，你可以给它提供默认的实现。因此你不需要改变你现在的代码。如果你往接口中添加方法，那么你必须改变实现该接口的类。
12、接口的意义？
规范、扩展、回调。


#### 泛型原理

#### 反射

#### 深拷贝浅拷贝

#### 线程/进程

##### 线程状态

##### 线程关闭及内存泄漏问题

#### 静态/动态代理

#### Java中对象的生命周期

#### 类加载过程

#### wait、sleep、notify

### JVM

#### JVM内存区域

#### Jvm内存模型

#### 引用类型及使用场景

#### 垃圾回收

##### GC算法

###### 可达性分析

###### 标记清除

###### 复制算法

###### 标记整理

###### 分代收集

###### 总结算法特点，以及适用场景

##### 新生代/老年代/永久代

##### 常见垃圾收集器使用场景及优缺点

#### 类加载器

#### jvm调优

### 并发

#### 原子性/可见性

#### sychronrized/volatile

##### 类锁，方法锁，重入锁

#### 手写单例模式

##### 不同单例写法

##### kotlin写法

#### 锁类型

##### 偏向锁、轻量级锁、重量级锁

##### ReentrantLock

###### 公平锁/非公平锁

##### 乐观锁/悲观锁

##### 锁自旋

##### 死锁概念，如何产生如何避免

##### CAS

##### AQS

#### 总结对比不同锁的实现方式及优劣

#### 线程池

##### 线程池类型

###### 工作队列实现，哪种容器，使用原因

## 数据结构

### Android优化数据结构

#### SparseArray

#### ArrayMap

#### ArraySet

#### 总结优化的对方

### 传统数据结构

#### 数组

##### ArrayList

##### LinkedList

##### CopyOnWriteArrayList

#### 队列

##### 常用类

###### PriorityQueue/PriorityBlockingQueue（volley/线程池有用到）

###### ConcurrentLinkedQueue 

####### CAS实现及原理

##### 使用场景及优缺点

#### 链表

#### 散列表

##### HashMap

###### 扩容原理

###### 1.8引入红黑树

###### hash生成

###### 其他优化

##### HashSet

##### HashTable

##### LinkedHashMap

###### Lrucache

##### ConcurrentHashMap

###### 1.7分段锁，1.8CAS，同步方式的演变

#### 树、堆、图、字典树

## 算法

## 网络基础

### 网络分层

### Socket

### TCP/UDP

### HTTP/HTTPS

#### 原理

#### Http1.1和Http1.0及2.0的区别

#### request/response构成

#### Https 请求慢的解决办法

1、不通过DNS解析，直接访问IP
2、解决连接无法复用
http/1.0协议头里可以设置Connection:Keep-Alive或者Connection:Close，选择是否允许在一定时间内复用连接（时间可由服务器控制）。但是这对App端的请求成效不大，因为App端的请求比较分散且时间跨度相对较大。

方案1.基于tcp的长连接 (主要） 移动端建立一条自己的长链接通道，通道的实现是基于tcp协议。基于tcp的socket编程技术难度相对复杂很多，而且需要自己定制协议。但信息的上报和推送变得更及时，请求量爆发的时间点还能减轻服务器压力（避免频繁创建和销毁连接）

方案2.http long-polling 客户端在初始状态发送一个polling请求到服务器，服务器并不会马上返回业务数据，而是等待有新的业务数据产生的时候再返回，所以链接会一直被保持。一但结束当前连接，马上又会发送一个新的polling请求，如此反复，保证一个连接被保持。 存在问题： 1）增加了服务器的压力 2）网络环境复杂场景下，需要考虑怎么重建健康的连接通道 3）polling的方式稳定性不好 4）polling的response可能被中间代理cache住 ……

方案3.http streaming 和long-polling不同的是，streaming方式通过再server response的头部增加“Transfer Encoding:chuncked”来告诉客户端后续还有新的数据到来 存在问题： 1）有些代理服务器会等待服务器的response结束之后才将结果推送给请求客户端。streaming不会结束response 2）业务数据无法按照请求分割 ……

方案4.web socket 和传统的tcp socket相似，基于tcp协议，提供双向的数据通道。它的优势是提供了message的概念，比基于字节流的tcp socket使用更简单。技术较新，不是所有浏览器都提供了支持。

3、解决head of line blocking
它的原因是队列的第一个数据包（队头）受阻而导致整列数据包受阻

使用http pipelining，确保几乎在同一时间把request发向了服务器

#### https能否被拦截

## kotlin

### 基础语法

### 常用关键字使用场景及实现原理

### 扩展方法/内联方法实现原理

## python

## flutter

## 自动化测试
