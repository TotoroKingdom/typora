# JUC

## JUC关键字

### synchronized，当一个线程进入到同步代码块时，会获取到当前的锁，而这时如果其他使用同样的锁的同步代码块也想执行内容，就必须等待当前同步代码块的内容执行完毕，在执行完毕后会自动释放这把锁，而其他的线程才能拿到这把锁并开始执行同步代码块里面的内容。

##### 1-修饰类

```java
 synchronized (Main.class){
     i++;
 }
```

##### 2-修饰具体的对象

```java
Thread01 main = new Thread01();
synchronized (main){
	i++;
}
```

##### 3-修饰方法

```java
private static synchronized void add() {
    value++;
}
```