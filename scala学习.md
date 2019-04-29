##  1. java、python、scala基本语法比较
##### 1.1 变量（都是指内存中的一个存储区域，该区域都有自己的名称-变量名。都只能由数字、字母、和下划线组成，且不能以数字打头）
* Python 使用变量前必须给变量赋值，赋值后该变量才会被创建，python变量没有默认值。python变量没有具体的类型，我们所说的"类型"是变量所指的内存中对象的类型。
```
x = 3           #整型变量
x = 10.0        #浮点型变量
x = "string"    #字符串变量
```

* java 变量使用前必须先声明，如果不赋值系统将按默认值进行初始化。变量类型  变量名 = 初始值
> 声明方式： 变量类型 变量名 = 初始值    

* scala  中使用var常量或者val变量声明变量， Scala 中声明变量和常量不一定要指明数据类型，在没有指明数据类型的情况下，其数据类型是通过变量或常量的初始值推断出来的。
所以，如果在没有指明数据类型的情况下声明变量或常量必须要给出其初始值，否则将会报错。
```
var x = 3
var x : Int = 3
val x = "string"
val x : String = "tring"
```
---
##### 1.2 数据类型
 * Python3 中有六个标准的数据类型：
```
Number（数字）
String（字符串）
List（列表）
Tuple（元组）
Set（集合）
Dictionary（字典）
Python3 的六个标准数据类型中：
不可变数据（3 个）：Number（数字）、String（字符串）、Tuple（元组）；
可变数据（3 个）：List（列表）、Dictionary（字典）、Set（集合）。
```

* java 分八大基本数据类型和引用数据类型
```
八大基础数据类型:byte、short、int、long 、float、 double、 boolean、 char
引用类型指向一个对象，指向对象的变量是引用变量。这些变量在声明时被指定为一个特定的类型，比如 Employee、Puppy 等。变量一旦声明后，类型就不能被改变了。
1. 对象、数组都是引用数据类型。
2. 所有引用类型的默认值都是null。
3. 一个引用变量可以用来引用任何与之兼容的类型。
```

* scala有着和java一样的数据类型，却别在于scala的数据类型首字母为大写
```
数据类型	描述
Byte	8位有符号补码整数。数值区间为 -128 到 127
Short	16位有符号补码整数。数值区间为 -32768 到 32767
Int	32位有符号补码整数。数值区间为 -2147483648 到 2147483647
Long	64位有符号补码整数。数值区间为 -9223372036854775808 到 9223372036854775807
Float	32 位, IEEE 754 标准的单精度浮点数
Double	64 位 IEEE 754 标准的双精度浮点数
Char	16位无符号Unicode字符, 区间值为 U+0000 到 U+FFFF
String	字符序列
Boolean	true或false
Unit	表示无值，和其他语言中void等同。用作不返回任何结果的方法的结果类型。Unit只有一个实例值，写成()。
Null	null 或空引用
Nothing	Nothing类型在Scala的类层级的最低端；它是任何其他类型的子类型。
Any	Any是所有其他类的超类
AnyRef	

上表中列出的数据类型都是对象，也就是说scala没有java中的原生类型。在scala是可以对数字等基础类型调用方法的
```
##### 1.3 数组
* python
```
序列是Python中最基本的数据结构。序列中的每个元素都分配一个数字 - 它的位置，或索引，第一个索引是0，第二个索引是1，依此类推。
Python有6个序列的内置类型，但最常见的是列表和元组。
序列都可以进行的操作包括索引，切片，加，乘，检查成员。
此外，Python已经内置确定序列的长度以及确定最大和最小的元素的方法。
列表是最常用的Python数据类型，它可以作为一个方括号内的逗号分隔值出现。
列表的数据项不需要具有相同的类型
创建一个列表，只要把逗号分隔的不同的数据项使用方括号括起来即可。如下所示：

list1 = ['Google', 'Runoob', 1997, 2000];
list2 = [1, 2, 3, 4, 5 ];
list3 = ["a", "b", "c", "d"];
与字符串的索引一样，列表索引从0开始。列表可以进行截取、组合等
```

* java J语言中提供的数组是用来存储固定大小的同类型元素。

> 你可以声明一个数组变量，如 numbers[100] 来代替直接声明 100 个独立变量 number0，number1，....，number99。
```
      // 定义数组
      double[] myList = new double[5];
      // 或者
      double[] myList2 = {1,2,3,4,5,6};
      myList[0] = 5.6;
      myList[1] = 4.5;
      myList[2] = 3.3;
      myList[3] = 13.2;
      myList[4] = 4.0;
      // 计算所有元素的总和
      double total = 0;
      for (int i = 0; i < size; i++) {
         total += myList[i];
      }
      System.out.println("总和为： " + total);
```
* scala 声明数组变量并不是声明 number0、number1、...、number99 一个个单独的变量，而是声明一个就像 numbers 这样的变量，然后使用 numbers[0]、numbers[1]、...、numbers[99] 来表示一个个单独的变量。数组中某个指定的元素是通过索引来访问的。
```
3种创建数组的方式
1. var z:Array[String] = new Array[String](3)
2. var z = new Array[String](3)
3. var z = Array(1, 1.2, 4,7)
 //示例
 def main(args: Array[String]) {
      var myList = Array(1.9, 2.9, 3.4, 3.5)
      
      // 输出所有数组元素
      for ( x <- myList ) {
         println( x )
      }

      // 计算数组所有元素的总和
      var total = 0.0;
      for ( i <- 0 to (myList.length - 1)) {
         total += myList(i);
      }
      println("总和为 " + total);

      // 查找数组中的最大元素
      var max = myList(0);
      for ( i <- 1 to (myList.length - 1) ) {
         if (myList(i) > max) max = myList(i);
      }
      println("最大值为 " + max);
    
   }
```
* 总结
1. java和scala中的数组元素必须是一致的，python中列表的数据类型可以不一致
2. java定义数组使用大括号{}，python定义数组使用中括号[]，scala定义数组使用小括号()






