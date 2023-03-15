# JavaSE

## 写在前面

这是我第三次复习java基础，前几次都是不怎么完全复习或者是学完之后效果也不怎么好。今天开始重新java基础。希望15天左右，能给我打好基础。因为时间的确不是很多，也不是很够用了。寒假计划还有一个SpringBoot 然后附带一个LInux。时间的确不是很多开始吧。

580 423 157 

![image-20230127171309636](http://images.japstylish.top/469cba537708ce5f5faf20bdb5bc01406ee57766.png)

---



## 转义字符

![image-20221230162721470](http://images.japstylish.top/6422928bf53e95b3a54c8121f00353088dabf0d8.png)

## 变量

概念：变量相当于内存中一个数据单元的表示，也就是在内存中有这么一个数据单元，它由 类型 + 名称 + 值组成的。我们可以通过变量名来访问到变量值。

用法：先声明，再使用。

## 程序中加号的使用

1.当左右两边都是数值型的时候，做加法运算。

2.当左右两边有一边为字符串的时候，做拼接运算。

```java
System.out.println("13-1="+12);
System.out.println(12+12);
```

---



# 第二章：Java数据类型

![image-20221229160123879](https://i0.hdslb.com/bfs/album/d3525e16823d7cc0cfcb72929cb6e38431584f3e.png)

* 浮点型

对于浮点型需要注意：浮点型默认类型是double类型的，如果要用float需要后面加一个f 

对于浮点型也是不可以进行比较，因为两个可能一方会有着精度上的丢失，容易造成误判。

* 字符型

在java中char的本质是一个整数，在默认情况下输出时，是Unicode对应的数值。

char类型是可以运算的，在运算中，char类型的字符会先转成unicode码，然后再参与运算。

---



## 基本数据类型转换

![image-20221230180408990](https://i0.hdslb.com/bfs/album/051762a968236e6053c20aace82c439dd9146b6c.png)

自动类型转换：小的往大的转，上图两条路线。

* 强制类型转换

自动类型转换的逆过程，就是将容量大的转换为容量小的类型的过程，但是有可能造成精度降低或者溢出。

* 强制类型转换符（）

---

* String类型的数据转换

1. **基本数据类型转换为String类型的**

演示：

```java
 float b = 1.33f;
 String bb = 1.33f + "";
```

2. **String类型转换为基本数据类型**

通过包装类parse来做到

演示：

```java
String s5 = "123";
 int s = Integer.parseInt(s5);
 String k5 = "123";
 float k = Float.parseFloat(k5);
```

---



## 运算符

* **算数运算符**

![image-20221231164241625](https://i0.hdslb.com/bfs/album/9a565cfc443f219f7d043507c0695be32de84cbe.png)

1）除法

演示：

```java
1.System.out.println(10/4);
输出结果：2 
如果两个整数数相除，结果肯定会保留一个整数
    
2.System.out.println(10/4.0);   
输出结果：2.5
如果两个数相除，想要得到高精度的，必须除数与被除数要带一个高精度的
```

2）取余

演示：

```java
System.out.println(10%3);
System.out.println(-10%3);
System.out.println(10%-3);

结果：
    1
   -1
    1
原因是：%的本质是a%b=a-a/b*b
```

3） 自增

1. **独立各自使用**

* i++ 

* ++i

作为独立的语句使用，两者含义一样，都等同于 i+1

2. **作为表达式使用**

* i++ ：先赋值，后自增 （ j=i++ 等同于 j=i i=i+1 ）
* ++i :  先自增，后赋值 （ j=++i 等同于 i=i+1 j=i ）

问题：如果 i = i++ 或者 i = ++i时 

![image-20221231172916259](https://i0.hdslb.com/bfs/album/6dfb61d0bb2e2d66201349cdc540ea8afaeb2023.png)

---



* **关系运算符**

![image-20221231180921212](https://i0.hdslb.com/bfs/album/3462cf63ef4f95f5db68be263d8da7e2a1ff28ab.png)

结果是一个Boolean值

---

* **逻辑运算符**

用于连接多个条件（多个关系表达式），最终结果是一个Boolean值

![image-20230103162055990](https://i0.hdslb.com/bfs/album/4d3415fd444abd2952f169cf0b70c196c6d5d817.png)

![image-20230103162444024](https://i0.hdslb.com/bfs/album/497b59718f3e3455e7c4f4bc7fa16e4084a560bd.png)

![image-20230103162458656](https://i0.hdslb.com/bfs/album/743a0f5d52793d1d17d3c504f1ae6438a1f33e8f.png)

* **赋值运算符**

a=a+b 等价于 a+=b

* **三元运算符**

基本形式：条件表达式 ? 表达式1：表达式2；

**运算规则：**

1. 如果条件表达式运算结果为True ，运算后的结果为表达式1
2. 如果条件表达式运算结果为False，运算后的结果为表达式2

```java
int a=22;
int b =10;
int c = a > b ? a++:b--;
System.out.print(a);
```

---



## 标识符

**标识符的概念**：在java中凡是可以取名的地方都可以称之为标识符，可以是一个变量、一个类、一个对象名称。

![image-20230105154119686](https://i0.hdslb.com/bfs/album/ddea9a1aadc991ecce39d99186cf47b1f79b5046.png)

**规范：**

![image-20230105154505284](https://i0.hdslb.com/bfs/album/dc9ece1ab80d567805ccfe7764ec33cc381b6eb9.png)

---

## 键盘输入语句：Scanner

```java
Scanner scanner = new Scanner(System.in);
System.out.println("请输入a")
String a = scanner.next()
```

## 字符串比较：equals

# 第三章 ：顺序、循环语句



## 分支结构

* if-else
* switch

## Switch

![image-20230107163021661](https://i0.hdslb.com/bfs/album/602af18003c3ee2b393b2acffe5bfe374ba2c357.png)

```java
   /**
         * switch 语法的使用
         */
        //1.接收字符
        Scanner scanner = new Scanner(System.in);
        char friday = scanner.next().charAt(0);
        switch (friday){
            case 'a':
                System.out.println("今天是星期一");
                break;
            case 'b':
                System.out.println("今天是星期二");
                break;
            case 'c':
                System.out.println("今天是星期三");
                break;
            default:
                System.out.println("您输入的有误");
        }

```

Switch注意事项

* **表达式数据类型应该和case后面常量的类型保持一致。如果没有一致，也应该case后面的常量类型可以转换为表达式数据类型 例如：switch（char）{case 20}**
* **Switch中表达式的返回值必须是这些{byte 、short 、int 、char 、enum 、String}**
* **case子句中的值必须是常量，而不能是变量**
* **default子句是可选的，也可以没有**
* **如果没有break语句，程序会直接运行到结尾，除非遇到一个break语句，如果此时匹配到了一个case 那么将运行完所有的case的子语句，不会经过case的判断条件**

## 循环语句

do-while for while

**do-while**

要点：

1. 先执行，后判断：也就是至少会执行一次。

```java
  public static void main(String[] args) {
        /**
         * doWhile 循环
         * 打印 1-100
         * 打印 1-100的和
         */
        int i = 1;
        int k = 0;
        do {
            System.out.println(i);
            i++;
            k+=i;
           }
        while (i<=100);
        System.out.println("1-100所有的数的和为:"+k);
    }
}
```

## 跳转控制语句：break

![image-20230108203508052](https://i0.hdslb.com/bfs/album/bc3abe75f98dd8fec250ad647df9839575af25f8.png)

![image-20230108210657013](https://i0.hdslb.com/bfs/album/1e5a0056b9a9519e3cf3d1f7dba89ed64d91b4ee.png)

## 跳转控制语句：continue

![image-20230108215942424](https://i0.hdslb.com/bfs/album/d3c449839b64c328d27f9832bd78fe741500dd74.png)

## 跳转控制语句：return

![image-20230108221630878](https://i0.hdslb.com/bfs/album/2bda7ff2b33a5086a3b9fa092c32085704680036.png)



# 第三章：数组

## 一维数组

![image-20230109173327419](https://i0.hdslb.com/bfs/album/26da94b9ddc66d25a665c45aa7d598cad689de06.png)

数组概念：数组可以存放**多个同一类型**的数据。数组也是一种数据类型，是引用类型。

![image-20230109180033245](https://i0.hdslb.com/bfs/album/dd6d8175cd84aac73e5f31165cbe60d502e2aaa1.png)

![image-20230109185648169](https://i0.hdslb.com/bfs/album/56ba5bbb6560675d93eb8ad870109af6c55eb488.png)

## 数组遍历：for循环中使用length

**具体说明：**

数组的动态初始化的第一种用法：

```java
double [] scores = new double[5];
double [] scores = new double[][2,3,4];
```

第二种用法：先声明，再分配空间

```java
double [] scores;
scores = new double[5];
```

![image-20230109193100495](https://i0.hdslb.com/bfs/album/dff5f74008fc5cdb46f0b35117a8748f246ad937.png)

## 数组赋值机制

![image-20230110161212882](https://i0.hdslb.com/bfs/album/d4e9d14ed0f04cb4d112565f9dd7aa8b8c14baf7.png)

```java
 int [] arr1 = {1,23,34};
        int [] arr2;
        arr2 = arr1;
        arr2[0] = 10;
        for (int i=0;i<arr1.length;i++ )
        {
            System.out.println(arr1[i]);
        }
```

**arr1的值变成了 {10,23,34}；**

## 值传递和引用传递的区别

![image-20230110162200345](https://i0.hdslb.com/bfs/album/9e9d559df23c6cc94601eb5992a014bdb072692c.png)

## 数组变化

#### 1.数组拷贝

```java
  /**
         * 数组拷贝
         */
        int [] arr1 = {1,2,3,4};

        //1.创建一个新的数组，开辟arr1 相同的空间
        int [] arr2 = new int[arr1.length];

        //2.遍历arr1 把 arr1赋值给 arr2
        for (int i=0;i<arr1.length;i++)
        {
            arr2 [i] = arr1[i];
        }
             arr2[0] = 10;
        for (int j =0;j<arr1.length;j++)
        {
            System.out.println("这是arr1的第"+(j+1)+"号元素"+arr1[j]);

        }
        System.out.println();
        for (int k = 0;k< arr2.length;k++)
        {
            System.out.println("这是arr2的第"+(k+1)+"号元素"+arr2[k]);
        }

```

#### 2.数组翻转

```java
public class ArrayReverse02 {
//编写一个 main 方法
public static void main(String[] args) {
//定义数组
int[] arr = {11, 22, 33, 44, 55, 66};
//使用逆序赋值方式
//老韩思路
//1. 先创建一个新的数组 arr2 ,大小 arr.length
//2. 逆序遍历 arr ,将 每个元素拷贝到 arr2 的元素中(顺序拷贝)
//3. 建议增加一个循环变量 j -> 0 -> 5
int[] arr2 = new int[arr.length];
//逆序遍历 arr
for(int i = arr.length - 1, j = 0; i >= 0; i--, j++) {
arr2[j] = arr[i];
}
//4. 当 for 循环结束，arr2 就是一个逆序的数组 {66, 55, 44,33, 22, 11}
//5. 让 arr 指向 arr2 数据空间, 此时 arr 原来的数据空间就没有变量引用
// 会被当做垃圾，销毁
arr = arr2;
System.out.println("====arr 的元素情况=====");
//6. 输出 arr 看看
for(int i = 0; i < arr.length; i++) {
    System.out.print(arr[i] + "\t");
}
}
}
```

#### 3.数组扩容

#### 4.数组缩减

## 冒泡排序

![image-20230110193235350](https://i0.hdslb.com/bfs/album/750f1c3dc717be9b8c5f98452d47dcdb719d38b1.png)

![image-20230110230502587](https://i0.hdslb.com/bfs/album/860d77c3ec6c6f227292659bec5ce4f3b007d1ac.png)

```java
 int [] a = {23,34,45,68,98,21};
        int temp = 0;
        for (int i = 0;i< a.length-1;i++)
        {
            for (int j =0;j< a.length-1-i;j++)
            {
                if (a[j]>a[j+1])
                {
                    temp = a[j+1];
                    a[j+1] = a[j];
                    a[j] = temp;
                }
            }
        }
        for (int k =0;k< a.length;k++)
        {
            System.out.print(a[k]+"\t");
        }
```

这种方法只不过是把原本要要比较 很多次的代码放到了循环里面。

## 二维数组

二维数组相较于一维数组来说 没有太大的区别 

初始化方式

静态初始化 

```java
int arr [] [] = {{3,4,5,2},{1,3,4,5}}
```

动态初始化 

```java
int arr [][] = new int[i][j];
```

其中，i代表这个二维数组中有几个一维数组，j代表着一个一维数组中含有几个元素。

## 二维数组的遍历

```java
   int [][] arr = new int[2][3];
        for (int i =0;i< arr.length;i++)
            for (int j =0;j< arr[i].length;j++)
            {
                System.out.println(arr[i][j]);
            }
```

# 第四章 ：类与对象

## 属性和行为

**一个对象包括它的属性与行为**

* **属性**

可以是颜色、性别、年龄、姓名等

* **行为**

可以是奔跑、沸腾、跳跃、撕咬等

说明一下，创建一个对象、实例化一个对象、把类实例化都是一个意思。

#### 1.属性或成员变量

从概念上将，属性等于成员变量，两者相等

```java
 static class Cat{
        int age;
        String name;
        String color;
        String [] arrs;//属性可以是基本数据类型，也可以是引用数据类型
```

#### 2.类和对象的内存分配机制

* **java内存结构分析**

![image-20230114210619172](https://i0.hdslb.com/bfs/album/ee449dd19d145f88c9ed09c0e0ef2a5396c04ad4.png)

![image-20230114210645454](https://i0.hdslb.com/bfs/album/4d94763fe761e7ba61d4d88d556df47fa8b7417e.png)

#### 3.方法

![image-20230115095448042](https://i0.hdslb.com/bfs/album/11dc8fe3d2e5cd91221dc50df87704cdeebfb852.png)

#### 4.形参与实参

**形参的理解：形参是为了方便，更好的使用变量引入的。**

![image-20230115093315281](https://i0.hdslb.com/bfs/album/aa12a74041eaf9db117f2d5834a93f9acab4de99.png)

```java
public class Demo05 {
    public static void main(String[] args) {
        Math math = new Math();
        math.Keep(5);
    }

       static class Math{
        int age;
        //使用形参
        public void Keep(int n){
            int sum =0;
            for (int i = 0;i<n;i++)
            {
                sum+=i;
            }
            System.out.println(sum);
        }

```



![image-20230115000041078](https://i0.hdslb.com/bfs/album/0f8d9df70d578d4b154c5a76b40921f8a2429a12.png)

如果返回的值不止一个，可以使用数组作为返回值。

```java
  public static void main(String[] args) {
        A a = new A();
        int[] sumAndDet = a.getSumAndDet(12, 34);
        System.out.println("两个数的和"+sumAndDet[0]);
        System.out.println("两个数的差"+sumAndDet[1]);

    }
    static class A{
        public int[] getSumAndDet(int n1,int n2){
            int [] arr = new int[2];
            arr[0] = n1+n2;
            arr[1] = n1-n2;
            return arr;
        }
```

#### 5.传参机制

1. **基本数据类型的传参机制**

![image-20230115120840206](https://i0.hdslb.com/bfs/album/dd9d94d53a3c4d724d39f242d2a2a2b6ea70e0f1.png)

```java
 public static void main(String[] args) {
        int a =10;
        int b =20;
        AA aa = new AA();
        aa.demo(a,b);
        System.out.println("主方法中a的值："+a+" b的值："+b);

    }
    static class AA{
        public void demo(int n1,int n2){
            int temp =n1 ;
            n1 = n2;
            n2 = temp;
            System.out.println("转换后a和b的值"+"\n"+"n1的值为："+n1+" n2的值为"+n2);

        }
```

2. **引用类型的传参机制**

**引用类型的传递，传递的是地址。可以通过形参来影响实参。**

![image-20230115131551569](https://i0.hdslb.com/bfs/album/70188c399f0672be609c5f4c866da7ca80dbf0c0.png)

传参机制：

当形参是一个对象时：

类中假如使对象=null；此时主方法中对象的属性并不会因此而改变，会继续输出。

类中假如新创建了一个对象，此时主方法中对象的属性也不会因此而改变，也会继续输出。

## 递归

![image-20230115154137329](https://i0.hdslb.com/bfs/album/d46991adc3c3ada48c3f430444c95be441826d48.png)

![image-20230115164720003](https://i0.hdslb.com/bfs/album/d207651c1c29e73d5edb56d038b2f90d5d04cccf.png)

我自己的结论：递归我觉得已经到那种稍微有一点算法了那种程度，我开始详细解读一下上图。

1. 首先最下面的是主栈，主栈在运行的时候，会遇到factorial这个方法，（只有有方法就开辟新栈），然后就有了上面的栈。
2. 在运行到最顶层的时候，便开始返回，递归都是从最顶层开始返回的。这里：**返回到哪里？返回到调用它的地方，也就是产生栈的源头，你这个栈是因为什么产生的，就返回到哪里！如图，就是返回到了f() 里面的值 **

![image-20230115173318154](https://i0.hdslb.com/bfs/album/3d1a9ec62db11610ca620f1c82f828602a25ae21.png)

## 重载

![image-20230115173703657](https://i0.hdslb.com/bfs/album/03698b239a437bf887bc139e0d3fdf6aeffc6d65.png)

语法介绍：

![image-20230115174642786](https://i0.hdslb.com/bfs/album/6245ce4cc7657f152b66ce2ef12e120aae48a9a1.png)

**四个方法名称一样，但是形参列表不同。构成重载。**

![image-20230115174833919](https://i0.hdslb.com/bfs/album/a9b7a495979b2c7b9bde85c516b6852403847088.png)

## 作用域

![image-20230115183116053](https://i0.hdslb.com/bfs/album/9d95529ac408cd05d827418dd4a1438e8f920d6d.png)

**全局变量、局部变量**

全局变量可以在全局使用，局部变量只能在方法体内部使用。

```java
 static class Cat{
        int age = 10;

        public void Cry(){
            String name = "jack";
            System.out.println(name);
        }
        public void Run(){
            System.out.println(age);
            System.out.println(name);//局部变量
        }
    }
```

## 构造器/构造方法

**constructor**

![image-20230115194245392](https://i0.hdslb.com/bfs/album/3dc8e03907caf0b68e894da2731c46b8f76fcd39.png)

![image-20230115194207134](https://i0.hdslb.com/bfs/album/36e56e6142bb4a08130422eddf8db427e9f2ce70.png)

![image-20230115210703675](https://i0.hdslb.com/bfs/album/60ac6544c76d4e99d37b1d871688df418a8f95f7.png)

## static关键字

static 可以修饰属性（成员变量）---：静态变量

​                                   常量称为   ---：静态常量

​                                    方法称为  ---：静态方法

它们统称之为：静态成员

static修饰的方法，不需要依赖对象来进行访问，只要这个类被加载，java虚拟机就可以通过类名找到它们。语法如下

```apl
类名.静态成员
```

**注意：**

- static 修饰的成员变量和方法，从属于类。
- 普通变量和方法从属于对象。
- 静态方法不能调用非静态成员，编译会报错。

# 第五章 JavaSE中级

## 包的命名

**一般是com.公司名.项目名.业务模块名**

## 访问修饰符

![img](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9yYXcuZ2l0aHVidXNlcmNvbnRlbnQuY29tL0pvdXJXb24vaW1hZ2UvbWFzdGVyL0phdmElRTUlOUYlQkElRTclQTElODAlRTglQUYlQUQlRTYlQjMlOTUvSmF2YSVFOCVBRSVCRiVFOSU5NyVBRSVFNCVCRiVBRSVFOSVBNSVCMCVFNyVBQyVBNi5wbmc?x-oss-process=image/format,png)

## 封装

![image-20230117204450250](https://i0.hdslb.com/bfs/album/da0f9de7b27e15753d4715cf3e3bc636c996b2a1.png)

封装的作用：

* 隐藏实现细节，不用管方法怎么实现的，需要用到这个方法直接调用就行了。
* 可以对数据进行验证，保证安全合理。

![image-20230118122001720](https://i0.hdslb.com/bfs/album/3434c7450169b9a94242a36ef00ca0409c9bed74.png)

综上所述：封装等于 访问修饰符：private 因为有了private方法，所以添加属性就不能用之前的方法了，所以诞生出了 set 和 get方法；

![image-20230118175320251](https://i0.hdslb.com/bfs/album/d15db761a31e421da7b0c4022405fff2cfea320b.png)

因为如果直接加入构造器，那么封装的防护机制就会失效，那么就是直接在构造器中加入set方法，仍然可以使用set方法中的约束。

## 继承

![image-20230118180247096](https://i0.hdslb.com/bfs/album/fa221fba3bf7072d139ce1294962e0cf9abbc605.png)

子类跟父类分开，父类写共有的属性跟方法，子类只写自己特有的属性跟方法。

**继承细节：**

![image-20230118191155483](https://i0.hdslb.com/bfs/album/0180242b1b6727716571ec5423ac18c47d239b42.png)

子类想要访问父类的私有属性和方法，需要父类创建一个public方法，把属性放进去，使子类访问。

```apl
举个例子：
我在学生类中定义了一个属性 score（成绩）
这时候子类 小学生 访问不到这个属性 这个时候在父类中 加入一个名为ace方法 返回成绩
然后子类 调用这个方法 就可以得到成绩了
 public double ace(){
        return score;
    }
```



![image-20230118192238211](https://i0.hdslb.com/bfs/album/5639dfbe013285d4374a9dace9375fc5128cf291.png)

```apl
总所周知，构造方法是每个类都有的，在继承中，父类的构造器会被子类调用
```



![image-20230118211208836](https://i0.hdslb.com/bfs/album/48537cdb9f1e28e03261194e595e485378aca2b5.png)

**4.子类是不继承父类的构造器（构造方法或者构造函数）的，它只是调用（隐式或显式）。如果父类的构造器带有参数，则必须在子类的构造器中显式地通过 super 关键字调用父类的构造器并配以适当的参数列表。**

如果父类构造器没有参数，则在子类的构造器中不需要使用 **super** 关键字调用父类构造器，系统会自动调用父类的无参构造器。也可以直接**super（）；**

## Super关键字

![image-20230118215548611](https://i0.hdslb.com/bfs/album/357acd43db19aca392746703cde37caccf5badb1.png)

## 重写

![image-20230119162309851](https://i0.hdslb.com/bfs/album/60180092a7c553d353108f02e49795b0d0bc4935.png)

![image-20230119163701404](https://i0.hdslb.com/bfs/album/1c274478b1a3dea5b05cd7bb31dcd6915aea0cc6.png)

## 多态

![image-20230119194034360](https://i0.hdslb.com/bfs/album/9a70ea378049230c1189873f21e389860e2f425d.png)

**多态的前提：**两个对象（类）存在继承关系

**多态存在的三个必要条件**

* 继承
* 重写
* 父类的引用指向子类（向上转型）



## 向上转型

![image-20230120171602236](https://i0.hdslb.com/bfs/album/bb177b0f3014658529b7147a9803dbfb75287b98.png)

![image-20230120171927660](https://i0.hdslb.com/bfs/album/1c67b9cc6496ee9e8cd9a51fb69dad25aeabb90d.png)

**属性没有重写之说:**

当创建一个Animal（父类）然后一个子类Dog 在主方法中，向上转型 Animal animal = new Dog（）

此时 你能访问到的 

* **父类中所有的属性跟方法** （但是访问父类中的属性需要遵守访问修饰符，private肯定不能访问）
* **子类中所有跟父类相同的方法（子类中的属性不可以访问)**

## 向下转型

![image-20230120181619807](https://i0.hdslb.com/bfs/album/4b47fbc6f4b8bbc2a70593642fbb0155b625b1c5.png)

## 动态绑定机制（重要）

定义：实现多态的技术称为：动态绑定，**是指在执行期间判断所引用对象的实际类型**，根绝实际类型调用其相应的方法。

1. 当调用对象方法的时候，该方法会和该对象的内存地址（**也就是运行类型**）绑定
2. 当调用对象属性时，没有动态绑定机制，哪里声明，哪里使用。

## 多态的应用

#### 1.多态数组

```java
注意 这个仅仅为 创建对象数组的方式
Rider[] riders = new Rider[3];
        riders[0] = new Rider(22,"龙骑","骑士");
        riders[1] = new Rider(19,"帝骑","骑士");
        riders[2] = new Rider(28,"女骑","骑士");
```



![image-20230120210111023](https://i0.hdslb.com/bfs/album/1fde0715df2d0a4f165c289734cc2978943e10e5.png)

 #### 2.多态参数

**方法定义的形参为父类类型，实参类型允许为子类类型**

## Object类

![image-20230122124948611](https://i0.hdslb.com/bfs/album/30ac009e3f84db07cf7d263c85024518be69d2c6.png)

## ==和equals

==：

1. 可以判断基本数据类型，判断的依据就是值是否相等
2. 也可以判断引用类型，判断的依据是两者返回的对象是否相等

equals：

是Object类的子类，只能判断引用类型，默认判断的是指地址是否相等，子类往往重写该方法，用于判断内容是否相等。

在实际中，可以根据需要在类中重写equals方法，以实现目标效果。

```java
//    重写equals方法
    public boolean equals(Object obj){
        if (this == obj)
        {
            return true;
        }
        if (obj instanceof Person)
        {
            if ( this.age==((Person) obj).age&&this.name.equals(((Person) obj).name))
            {
                return true;
            }
        }
      return false;
    }

```

## 断点

![image-20230127231647129](https://i0.hdslb.com/bfs/album/cc2ba901f9da48817f83aedd3ae880a9afddb809.png)

# 第六章 Java高级部分

## 静态变量

![image-20230127163840196](https://i0.hdslb.com/bfs/album/d7e6e4c4ae7b2d5924e5b96cee06579b29053475.png)

![image-20230127163916438](https://i0.hdslb.com/bfs/album/4cfd4d2e9cef1768c18b6935e00bdefa5ab178e0.png)

#### 细节

![image-20230127165040894](https://i0.hdslb.com/bfs/album/0bb543c2e6a3fac17571140687481ba66323bc7f.png)

## 静态方法

![image-20230127165724383](https://i0.hdslb.com/bfs/album/c514b7844f88b34993d9f58b8577443435054525.png)

雷区：

1. 静态方法中不能使用非静态变量，也不能出现this关键字。

## Main方法

1. main方法是由java虚拟机来调用，所以访问修饰符是public 
2. main方法在执行的时候，不用创建对象，所以是static方法
3. 接受一个String类型的数组，可以传递参数
4. 传递参数可以在命令行中传递 格式是 类名 后跟 变量名称

## 代码块

![image-20230127175047820](https://i0.hdslb.com/bfs/album/871a145a443ba49934a83a44058432a5bc01725e.png)

## final关键字

![image-20230127204055949](https://i0.hdslb.com/bfs/album/d5e3b9020cffb4d51be333918f36b7dca589eb3e.png)

**使用细节**

1. final修饰的属性又叫常量 一般用XX_XX_XX来命名 如下：

```java
public static final String RETURN_OBJECT_CODE_SUCCESS="1";
```

2. final修饰的属性在定义时，必须赋初值，而且以后不能再修改 可以在

* **定义时，直接赋初值 如上面演示**
* **在构造器中赋值**
* **在代码块中赋值**

3. 如果final修饰的属性是静态的，则初始化的位置只能是

* **定义时**
* **在静态代码块中**

4. final类可以实例化对象，但是不可以继承

5. 在一个类中，如果类中方法含有final，则该方法不能被重写，但是可以被继承。
6. final不能修饰构造方法\构造器
7. final和static一起使用，效率更高。不会导致类加载，底层做了优化。

## abstract抽象类

![image-20230127210632868](https://i0.hdslb.com/bfs/album/f0e0ef3e2fe4aa455703ce2bb5ca8f991eadb7d7.png)

**细节**

1. 抽象类是不能被实例化的/创建对象
2. 抽象类不一定要包含抽象方法，也就是抽象类可以没有抽象方法
3. 一旦这个类中包含了abstract方法，则这个类必须声明为abstract
4. abstract只能修饰类和方法，不能修饰属性和其他

![image-20230127213638612](https://i0.hdslb.com/bfs/album/354fdcf56c0cd1ae92bb1c3e0cae0c613c794b58.png)

## 接口

![image-20230128102700600](https://i0.hdslb.com/bfs/album/143444425fd85a3e38d8bd27c1dfa485e1d2c69c.png)

1. 接口不可以被实例化
2. 接口中的方法都是public修饰，接口中的抽象方法可以不用static修饰
3. 一个普通类实现接口，就必须实现接口中的所有方法。
4. 抽象类实现接口，可以不用实现接口中的方法。

![image-20230128162930232](https://i0.hdslb.com/bfs/album/fdba49cd04a449bab71328fd9422239b354a05ee.png)

## 接口和继承

当子类继承父类时，就自动拥有了父类的功能

如果子类需要扩展功能，则需要接口的实现 ，可以说接口是对java单继承机制的一种补充。

## 内部类

![image-20230128174117654](https://i0.hdslb.com/bfs/album/606cbb2ca62832d54b8542a8665682d5da2a69c4.png)

## 内部类的分类

![image-20230128175721317](https://i0.hdslb.com/bfs/album/e70465a7ea15d84f929db30447a1796f9769a213.png)

 #### 1.局部内部类

说明：局部类是定义在外部类的局部位置，比如方法中，并且有类名。

1. **可以直接访问外部类的所有成员，包含私有的**
2. **不能添加访问修饰符，因为它的地位就是一个局部变量，因为局部变量就不可以使用访问修饰符，但是可以使用final 因为局部变量也可以使用final**
3. 作用域：仅仅在定义它的方法或代码块中
4. 内部类访问外部类的成员-->**直接访问**
5. 外部类访问内部类的成员-->**创建对象，在进行访问（在作用域中创建对象）**
6. 其他类不可以访问外部类的属性
7. 如果外部类和内部类的成员重名时，默认遵循就近原则，如果想访问外部类的成员，则可以使用（外部类名.this.成员）去进行访问 举例如下

```java
System.out.println("外部类的n2="+外部类名.this.n2)
```

#### 2.匿名内部类（最重要）

匿名内部类是定义在外部类的局部位置，比如是在方法中，并且没有类名

1.本质是类 2.没有类名 3.内部类 4.同时还是一个对象

![image-20230201122103861](http://images.japstylish.top/image-20230201122103861.png)

###### 2.1接口演示

前情提示：接口是一种规范，如果你想实现接口中的方法，就要写一个类去实现接口，但是仅仅想实现一次，只写一个类的话，非常麻烦，就出现了匿名内部类可以使用

```java
public class Demo03 {
    public static void main(String[] args) {
        A.Listener listener = new A.Listener();
        listener.keep();
    }
}

interface A {
        default void add(){
    }

class Listener{
    public void keep(){
        匿名内部类 同时还是一个对象 记得要加引号
     A i = new A(){
            @Override
            public void add() {
                System.out.println("我加你等于无敌");
            }
        };
     i.add();
    }
}
}

```

###### 2.2类的演示

```java
Father f =  new Father(12){
        @Override
        public void test() {
            System.out.println("father的测试类"+age);
        }
    };
    f.test();
    }
}

class Father{
    int age;

    public Father(int age) {
        this.age = age;
    }
    public void test(){

    }
}

```

###### 2.3匿名内部类的调用方法

两种

```java
  @Override
    public void test() {
        System.out.println("father的测试类"+age);
        System.out.println();
    }
};
father.test();
第一种调用方法
System.out.println(father.getClass());
}
```

```java
  new A(){
            @Override
            public void add() {
                System.out.println("我加你等于无敌");
            }
        }.add();
不用对象接受，直接调用。
```

![image-20230201162149489](http://images.japstylish.top/image-20230201162149489.png)

#### 3.成员内部类

![image-20230201162754730](http://images.japstylish.top/image-20230201162754730.png)

![image-20230201165116641](http://images.japstylish.top/image-20230201165116641.png)

#### 4.静态内部类

![image-20230201165224779](http://images.japstylish.top/image-20230201165224779.png)

![image-20230201165818235](http://images.japstylish.top/image-20230201165818235.png)

# 第七章 异常

## 异常

快捷键：ctrl+alt+t

**开发过程中语法错误和逻辑错误不算异常**

![image-20230201175550711](http://images.japstylish.top/image-20230201175550711.png)

![image-20230201214456132](http://images.japstylish.top/image-20230201214456132.png)

1. NullPointException 空指针异常

当应用程序试图在需要对象的地方使用null时，抛出该异常 （对象还没有创建，就去使用，可以不只是对象，也可以是属性）

## 异常处理机制

1、**try-catch-finally**

```js
  try {
//           把可能出现异常的代码放进去
        } catch (Exception e) {
//            1.如果有异常，那么将捕获异常
//            2.将异常封装到 Exception 对象 e中传递给catch
//            3.得到异常对象之后，程序员自己处理逻辑
              e.printStackTrace();
        } finally {
//            1.不管try中是否有异常发生 都要执行finally中的代码块
//            2.通常将释放资源的代码放入finally中

        }
    }
```

2、**throws**

![image-20230201225217508](http://images.japstylish.top/image-20230201225217508.png)

用法：方法中加入 throws exception

流程：f2中如果选择抛出异常，那么将会把异常返回给f1有两种选择，一种是 try-catch-finally，另外一种就是继续向上抛出异常。

## try-catch

![image-20230201231340265](http://images.japstylish.top/image-20230201231340265.png)

3、可以使用不同的异常类型来接受异常 比如

```js
 int num1 = 10;
            int num2 = 0;
            keep = num1/num2;
            System.out.println("伞兵一号");
        } catch (ArithmeticException e) {
//            e.printStackTrace();
            System.out.println(e.getMessage());
```

如果希望不管是否发生异常，都执行某段代码，则使用finally{ }（关闭链接、释放资源）

## throws

![image-20230202111640205](http://images.japstylish.top/image-20230202111640205.png)

![image-20230202160207617](http://images.japstylish.top/image-20230202160207617.png)

## 自定义异常

```java
 public static void main(String[] args) {
        int age = 123;
        if(!(age>10&&age<120))
        {
            throw new AgeException("年龄设置有误");
        }
        System.out.println("正确");

    }
}
class AgeException extends RuntimeException{
    public AgeException(String message) {
        super(message);
    }
}

```

**一般情况下，自定义异常都继承RuntimeException，即做成一个运行时异常。**

![image-20230202162113615](http://images.japstylish.top/image-20230202162113615.png)

# 第八章 常用类

## 包装类

**八种基本数据类型的引用类型——包装类**

![image-20230202171407582](http://images.japstylish.top/image-20230202171407582.png)

继承关系

![image-20230202172111951](http://images.japstylish.top/image-20230202172111951.png)

## 手动装箱与自动装箱

关于 包装类与基本数据类型之间的转换

```java
int n1 = 10;
// 自动装箱与手动装箱
    Integer k = Integer.valueOf(n1);
    Integer i = n1;
//自动拆箱与~
	int j = k.intValue();
	int g = k;

```

## 包装类与String的互相转换

```java
public class Wrapper_ {
    Integer n1 = 10;
//    包装类与String类型的互相转换
//    包装类-->String
//    1.第一种方式
    String i = n1+"";
//    2.第二种 用包装类中自带的toString方法
    String k = n1.toString();
//    3.第三种
    String m = String.valueOf(n1);

//    String-->包装类
    String ruler = "123";
    String rub = "123";
//    第一种 包装类中的方法
    Integer kk = Integer.parseInt(ruler);
//    第二种 直接new Integer
    Integer integer = new Integer(rub);
```

## 包装类常用方法

![image-20230202215644988](http://images.japstylish.top/image-20230202215644988.png)

## String类

String对象用来保存字符串，也就是一组字符序列

字符串常量对象是用双括号括起来的字符序列，一个字符不区分形式，都占两个字节。

#### 继承关系

![image-20230203103434725](http://images.japstylish.top/image-20230203103434725.png)

**Serializeable**：String实现这个接口，String对象可以在网络上进行传输

**Comparable**：对象之间可以相互比较。

#### 特征

**String类有很多的构造器，构成了构造器的重载**

![image-20230203112114625](http://images.japstylish.top/image-20230203112114625.png)

**String中的字符存储**

```java
 @Stable
    private final byte[] value;
    final类型，赋值之后就不能改变了（地址不可以改变）
        即value不能指向新的内容，但是单个字符可以改变。
```

#### 创建String的方式

![image-20230203115749256](http://images.japstylish.top/image-20230203115749256.png)

#### 常用方法

![image-20230203154757997](http://images.japstylish.top/image-20230203154757997.png)

![image-20230203155343471](http://images.japstylish.top/image-20230203155343471.png)

![image-20230203162148906](http://images.japstylish.top/image-20230203162148906.png)

**format**

占位符

1. %s，%d，%.2f，%c称为占位符

2. 这些占位符由后面的变量来替换

3. %s表示后面由字符串来替换

4. %d表示由整数来替换

5. %.2f表示由小数来替换。替换后只会保留小数点之后的两位，并且进行四舍五入的处理

format演示

![image-20230203165954108](http://images.japstylish.top/image-20230203165954108.png)

   ## StringBuffer

![image-20230203170621520](http://images.japstylish.top/image-20230203170621520.png)

   ![image-20230203170954661](http://images.japstylish.top/image-20230203170954661.png)

#### 结构图：

![image-20230203171840639](http://images.japstylish.top/image-20230203171840639.png)

#### 特征

父类：AbstractStringBuilder

2. StringBuffer实现了Serializable接口，即可以实现串行化
3. 存储的内容在父类，中 byte[] value;存储数据，但是不是final类型。数据放在堆中，不在常量池-----不用每次都更换地址（创建新的对象）
4. StringBuffer本事也是一个final类

![image-20230203172610408](http://images.japstylish.top/image-20230203172610408.png)

#### String与StringBuffer的相互转换

![image-20230203175253963](http://images.japstylish.top/image-20230203175253963.png)

#### 常用方法

![image-20230203175607566](http://images.japstylish.top/image-20230203175607566.png)

![image-20230203180724993](http://images.japstylish.top/image-20230203180724993.png)

 ![image-20230203180856992](http://images.japstylish.top/image-20230203180856992.png)

![image-20230203181004786](http://images.japstylish.top/image-20230203181004786.png)

## StringBuilder

![image-20230203204827078](http://images.japstylish.top/image-20230203204827078.png)

#### 常用方法

和StringBuffer一样，均代表可变的字符序列，两者使用起来方法是一样的，使用情况也一样，不一样的区别在于 StringBuffer适用于多线程，StringBuilder适用于单线程，StringBuilder效率更快一点。

## 三者总结

**String：不可变字符序列，效率低，但是复用率高。**

不可变字符序列就是，保存的字符串都放在常量区，存储的方法是final方法，地址不能更换，当你字符串比如要新加一个，就要开辟新的方法区地址。

为什么要说复用率比较高，OK，常量池中假如有一个lzz字符串，那么处在堆中的对象都可以指向lzz

![image-20230203222337756](http://images.japstylish.top/image-20230203222337756.png)

**StringBuffer：可变字符序列，效率较高，线程安全**

Stringbuffer，保存的是字符串变量，里面的值可以更改，每次更改内容，地址不改变。

线程是 StringBuffer中的方法都带有synchronized。

**StringBuilder**

可变字符序列，效率最高，线程不安全

![image-20230203224742598](http://images.japstylish.top/image-20230203224742598.png)

## Math类

![image-20230204153159707](http://images.japstylish.top/image-20230204153159707.png)

#### random

random是返回一个大于等于0，小于1的一个double类型的数 也就是【0,1）

公式：**(int)(a+Math.random()*(b-a+1))**

## Arrays类

主要是对数组进行操作

**toString**

```java
 Integer[]arrs = {1,34,45,5,-1};
 System.out.println(Arrays.toString(arrs));
```

**sort**

```java
 Integer[]arrs = {1,34,45,5,-1};
	Arrays.sort(arrs);
    System.out.println(Arrays.toString(arrs));
//  排序后：[-1, 1, 5, 34, 45]
```

![image-20230206143259081](http://images.japstylish.top/image-20230206143259081.png)

```java
// 可以通过实现一个接口，来实现定制排序 Comparator
Arrays.sort(arrs, new Comparator<Integer>() {
     @Override
     public int compare(Integer o1, Integer o2) {
       return o2-o1;
    }
 });
     System.out.println(Arrays.toString(arrs));
```

**binarySearch**

通过二分查找进行寻找数组里面是否有这个数，要求必须排好序

```c#
  System.out.println(Arrays.binarySearch(arrs,1));
```

**copyof**

![image-20230206145500615](http://images.japstylish.top/image-20230206145500615.png)

**fill**

![image-20230206145639402](http://images.japstylish.top/image-20230206145639402.png)

**equals**

![image-20230206145930719](http://images.japstylish.top/image-20230206145930719.png)

## System类

![image-20230206150250544](http://images.japstylish.top/image-20230206150250544.png)

## BigInteger和BigDecimal类

![image-20230206152823520](http://images.japstylish.top/image-20230206152823520.png)

![image-20230206153702276](http://images.japstylish.top/image-20230206153702276.png)

注意事项：当整型较大，long也保存不了的时候，需要用bigInteger保存比较大的整型，使用时需要创建对象，而且保存为字符串类型的。加减乘除也不能用普通的符号 需要用 add subtract ,,,,,,

BigDecimal同理

![image-20230206160331701](http://images.japstylish.top/image-20230206160331701.png)

# 日期类

**Date**

不过多解释

**Calendar**

```java
/*calendar是一个抽象类，并且构造器是私有的。
 可以通过getInstance()方法来获取实例        
 创建日历对象（不可以new出来 因为calendar是抽象的 不可以被实例化）*/ 
          Calendar instance = Calendar.getInstance();
          System.out.println(instance.get(Calendar.DAY_OF_YEAR));
```

![image-20230206171223644](http://images.japstylish.top/image-20230206171223644.png)

**第三代日期类**

前两代日期类每一代都有相应的问题，对于第一代，在jdk1,0版本就已经使用，到1,1版本基本已经废弃，开始使用calendar类。但是calendar类也有相对应的问题，例如不能处理闰秒（每两天增加一秒），月份从0开始等 所以在jdk1.8

**第三代日期常用方法**：

* LocalDate（日期/年月日）
* LocalTime（时间/时分秒）
* LocalDateTime（年月日时分秒）

LocalDate是包含日期，可以获取日期片段 LocalTime同理 **LocalDateTime同时包含日期和时间片段**

```java
// 创建方式：LocalDate.now();
LocalDateTime now1 = LocalDateTime.now();
        System.out.println(now1);
        System.out.println("年"+now1.getYear());
        System.out.println("月"+now1.getMonthValue());
        System.out.println("日"+now1.getDayOfMonth());
        System.out.println("周几"+now1.getDayOfWeek());
        System.out.println("时"+now1.getHour());
        System.out.println("分"+now1.getMinute());
        System.out.println("秒"+now1.getSecond());
```

**格式化方法**

**DateTimeFormatter**

```java
LocalDateTime now1 = LocalDateTime.now();
        DateTimeFormatter dt = DateTimeFormatter.ofPattern("YYYY年-MM月-dd日  HH:mm:ss ");
        String format = dt.format(now1);
```

**时间戳**

创建方式：

```java
Inatant.now()
```



![image-20230206175339176](http://images.japstylish.top/image-20230206175339176.png)

# 集合

**集合主要是两种集合（单列集合、双列集合）**

Collection接口有两个重要的接口，LIst-Set ，他们实现的子类都是单列集合，里面存放的都是单个元素

Map实现的子类是双列集合，里面存放的都是键值对 （key-value）类型的

![image-20230206191747461](http://images.japstylish.top/image-20230206191747461.png)

![image-20230206214300157](http://images.japstylish.top/image-20230206214300157.png)

## Collection

1. 实现了Iterable接口

```java
public interface Collection<E> extends Iterable<E> {
```

![image-20230208120244172](http://images.japstylish.top/image-20230208120244172.png)

2. Collection中的方法

```java
/**
add：添加单个元素
remove:删除指定元素
contains：查找元素是否存在
size：获取元素个数
isEmpty：判断是否为空
clear：清空
addAll：添加多个元素
containsAll：查找多个元素
removeAll：删除多个元素
```

## 遍历元素的方法

1. **Iterator（迭代器）**

* Iterator对象称之为迭代器，主要用于遍历Collection集合中的元素

使用方法：

```java
  Iterator iterator = list.iterator();
        while (iterator.hasNext()) { //用于判断集合里面是否还有元素
            Object next =  iterator.next();
            System.out.println("\t"+next);
        }
//(快捷键：itit)
显示所有快捷键 Ctrl+j
// 如要要求再次遍历 则需要重置迭代器 具体方法为：
   iterator = list.iterator();
    while (iterator.hasNext()) {
        Object next =  iterator.next();
```

2. for循环增强

可以代替inerator迭代器 特点：增强for循环就是inerator的简化版，本质一样，只能用于遍历集合或者数组。

基本语法

```java
/*
for（元素类型 元素名 ：集合或者数组名）
{
访问元素
}
*/
 for (Object i:list)
{
System.out.println(i);
}

```

## List类

1. list集合中元素添加的顺序和取出的顺序一致。
2. 集合中任何一个元素都支持索引（从0开始）

![image-20230208162601770](http://images.japstylish.top/image-20230208162601770.png)

Arraylist

![image-20230208174331506](http://images.japstylish.top/image-20230208174331506.png)

Vector

![image-20230208180213579](http://images.japstylish.top/image-20230208180213579.png)

#### ArrayList与LInkedList对比

|            | 底层结构 | 增删的效率        | 改查的效率 |
| ---------- | -------- | ----------------- | ---------- |
| ArrayList  | 可变数组 | 较低 数组扩容     | 较高       |
| LinkedList | 双向链表 | 较高 通过链表追加 | 较低       |

![image-20230208183340531](http://images.japstylish.top/image-20230208183340531.png)

## Set集合

![image-20230208185904018](http://images.japstylish.top/image-20230208185904018.png)

1. 无序（添加和取出的顺序不一致）
2. 没有索引，也就是不可以通过索引来获取数据等操作
3. 不允许重复元素 （只能有一个null）

![image-20230208210124745](http://images.japstylish.top/image-20230208210124745.png)

#### HashSet集合的加入机制

**HashSet的底层：HashMap** *HashMap的底层是（数组+链表+红黑树）*

```java
//      关于Hashset存放数据这件事
        HashSet hashSet = new HashSet();
        hashSet.add(new Person("zhang"));// True
        hashSet.add(new Person("zhang"));// True
        hashSet.add("zhang");//("只能加入一个")
        hashSet.add("zhang");
        hashSet.add(new String("huang"));//("只能加入一个")
        hashSet.add(new String("huang"));
        System.out.println(hashSet);

```

值得注意：在使用TreeSet的时候，不可以添加对象，会直接报错。

底层原理：

![image-20230209145108764](http://images.japstylish.top/image-20230209145108764.png)

解释：（数组加链表）把数组每一个索引的位置分为不同节点，然后加入元素，排列在下一个节点，当节点达到一定数量就形成树了。（存取效率很高）

#### Hash扩容机制

![image-20230209145616283](http://images.japstylish.top/image-20230209145616283.png)

#### LinkedHashSet

![image-20230209171744182](http://images.japstylish.top/image-20230209171744182.png)

继承了HashSet

## Map集合

![image-20230209174952476](http://images.japstylish.top/image-20230209174952476.png)



#### 常用方法

![image-20230209180259665](http://images.japstylish.top/image-20230209180259665.png)

#### 遍历方法

```java
 public static void main(String[] args) {
        Map map = new HashMap<>();
        map.put("1","管");
        map.put("2","与");
//      1.取出key
        Set keySet = map.keySet();
//      for循环增强
        Iterator iterator = keySet.iterator();
        for (Object key :keySet) {
            System.out.println(key+"="+map.get(key));
        }
        System.out.println("=======迭代器======");
//      迭代器
        while (iterator.hasNext()) {
            Object keybase =  iterator.next();
            System.out.println(keybase+"="+map.get(keybase));
        }
//       2.取出value
        Collection values = map.values();
//        增强for循环
        for (Object o :values) {
            System.out.println(o);
        }
//         迭代器
        Iterator iterator1 = values.iterator();
        while (iterator1.hasNext()) {
            Object next =  iterator1.next();
            System.out.println(next);

        }

```

```java
//使用entryset遍历
// 使用entrySet
//根据结论 entryset中元素就是entry 准确来说是Map.Entry 就先把entryset找出来 进行一个类型转换 然后调用里面的 getkey（） 和 getvalue（） 方法
        System.out.println("使用entrySet");
        Set entryset = map.entrySet();// entrySet<Map.Entry<key-value>>
        for (Object entry :entryset) {
            Map.Entry et = (Map.Entry) entry;
            System.out.println(et.getKey()+"-"+et.getValue());
        }
// 也可以使用迭代器
```



## HashMap

**1. HashMap是Map接口使用频率最高的实现类**

**2.HashMap是以Key-Value方式来存取数据的（HashMap$Node类型）*Entry 具体解释如下：***

****

![image-20230210142213892](http://images.japstylish.top/image-20230210142213892.png)

![image-20230210142258573](http://images.japstylish.top/image-20230210142258573.png)

![image-20230210142311908](http://images.japstylish.top/image-20230210142311908.png)

小结：

![image-20230210144327850](http://images.japstylish.top/image-20230210144327850.png)

#### HashMap的扩容机制

---

1. HashMap底层维护了Node类型的数组，默认为null
2. 当创建对象时，将加载因子（loadfactor）初始化为0.75
3. 当添加key-value时，通过key的哈希值得到在table处的索引，然后判断该索引处是否有元素，如果没有元素，则直接添加进去。如果索引处有元素，则继续判断该元素的key和准备加入的元素的key是否相等，如果相等，则直接替换。如果不相等，则要继续判断是数结构还是链表结构，做出相应处理，如果添加时，发现容量不够，则需要进行扩容。
4. 第一次添加，则需要扩容table的容量为16，临界值为12（16*0.75） 临界值为下一次扩容前要满足添加的条件 
5. 以后再次扩容，则需要扩容为table的容量为原来的2倍（32），临界值为原来的2倍（24）并以此类推
6. 在java8中 如果一条链表上的元素个数超过了（默认为8），且table的大小>=（默认为64）链表就会进化为红黑树

## Hashtable

![image-20230210153635958](http://images.japstylish.top/image-20230210153635958.png)

#### hashtable扩容机制

![image-20230210154843135](http://images.japstylish.top/image-20230210154843135.png)

## properties

![image-20230210161112935](http://images.japstylish.top/image-20230210161112935.png)

## tree

#### TreeSet(排序)

```java
 public static void main(String[] args) {
        TreeSet treeSet = new TreeSet(new Comparator() {
            @Override
            public int compare(Object o1, Object o2) {
//                return ((String)o1).compareTo((String)o2);
                return ((String)o1).length()-((String)o2).length();
            }
        });
        treeSet.add("dackf");
        treeSet.add("bucy");
        treeSet.add("co");
        treeSet.add("azz");
        System.out.println(treeSet);

    }
}

```

排序规则：

根据你添加的排序规则来定，如果你添加的规则为长度的话，那么底层就会进行循环查找，当你添加进去一个 三个长度的字符串之后，就插入不进去另外一个三个字符的的字符串了。

#### TreeMap（排序）

```java
  TreeMap treeMap = new TreeMap(new Comparator() {
            @Override
            public int compare(Object o1, Object o2) {
                return ((String)o1).compareTo((String)o2);
            }
        });
        treeMap.put("bbck","天外飞仙");
        treeMap.put("abck","天上天下");
        treeMap.put("ccck","天蓬元帅");
        treeMap.put("ddck","天天学习");
        System.out.println(treeMap);

```

## Collections工具类

![image-20230212104346803](http://images.japstylish.top/image-20230212104346803.png)

方法集

![image-20230212110125208](https://article.biliimg.com/bfs/article/202cab74268200bb454bfb8734e0fab35ee0c824.png)

![image-20230212111944762](https://article.biliimg.com/bfs/article/82f08b15dff1006fd0f609f0958e26c49d9af9fe.png)

## 选择

![image-20230210162441442](http://images.japstylish.top/image-20230210162441442.png)

# 泛型

![image-20230215155434863](http://images.japstylish.top/image-20230215155434863.png)

细节：

1. 泛型里面放进去的都是引用类型，不可以放基本数据类型
2. 如果是无关类的话，是不可以放入泛型中的，但是如果有继承关系则可以

## 自定义泛型



