    java.lang.Object
        java.util.Scanner 
###简介
java.util.Scanner是Java1.5的新特征，主要功能是获取控制台输入内容。

###声明
当通过new Scanner(System.in)创建一个Scanner，控制台会一直等待输入，直到敲回车键结束，把所输入的内容传给Scanner，作为扫描对象。

###官方实例
除了空格，我们还可以使用分隔符，下面这个例子从一个字符串中读取了多个

     String input = "1 fish 2 fish red fish blue fish";
     Scanner s = new Scanner(input).useDelimiter("\\s*fish\\s*");
     System.out.println(s.nextInt());
     System.out.println(s.nextInt());
     System.out.println(s.next());
     System.out.println(s.next());
     s.close();
     
输出以下内容:

    1
    2
    red
    blue

###主要方法
**nextInt()**，读取下一个int型标志的token.但是焦点不会移动到下一行，仍然处在当前行上。

**nextLine()**，读取当前行剩余的所有的内容，包括换行符"\n"，然后把焦点移动到下一行的开头。"\n"并不会成为返回的字符串值的一部分。

**next()**，以换行或者空格符为分界线接收下一个String类型变量。

**hasNextLine()** ，如果在此扫描器的输入中存在另一行，则返回 true。

**nextLong(int radix)** ，此方法返回从输入信息扫描的long值。如果下一个标记不能转换为有效的long值，此方法将抛出InputMismatchException异常。如果转换成功，则scanner执行匹配的输入。
