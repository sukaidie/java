##44. interface, Ma
- 类继承类
- 类实现接口
- 接口继承接口

```java
interface Valuable{
  public double getMoney();
}

interface Protectable{
  public void beprotected();
}

interface A extends Protectable{
  void m();
}

abstract class Animal{
  private String name;
  abstract void enjoy();
}

class GoldenMonkey extends Animal implements Valuable,Protectable{
  public double getMoney(){
    return 10000;
  }
  public void beprotected(){
    System.out.println("live in the room");
  }
  public void enjoy(){
    .......;
  }
  public void test(){
    Valuable v=new GoldenMonkey();//新建了一个金丝猴，但是以接口Valuable为视角，v里只有getMoney()方法
    v.getMoney();
    Protectable p=(Protectable)v;//把v强转成了以接口Protectable为视角，p里只有beProtectable()方法
    b.beProtected();
  }
}

class Han implements A{
  public void m(){}
  public void beProtected(){}
}
```


##10.01 网络
