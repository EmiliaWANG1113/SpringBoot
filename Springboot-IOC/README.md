# Springboot-IOC

## 控制反轉IOC（Inversion of Control，IOC）
* 控制反轉為一個設計思想 ，把對於某個物件的控制權移轉給第三方容器

ex:
A物件程式內部需要使用B物件 A,B物件中有依賴的成份

控制反轉是把原本A對B控制權移交給第三方容器

降低A對B物件的耦合性，讓雙方都倚賴第三方容器。

##### IOC優點：
1. 鬆耦合(Loose coupling)
2. 生命週期管理(Lifecycle Management)
3. 方便測試程式(More testable)

##### 使用方法(@Component)
* 用法：只能加在class上
* 用途：將該class變成由Spring容器所管理的object

```java
public class HpPrinter implements Printer{
    @Override
    public void print(String message){
         System.out.println("HP印表機： "+message);
    }
}
```

