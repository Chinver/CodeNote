
###题目描述

给定区间[-2的31次方, 2的31次方]内的3个整数A、B和C，请判断A+B是否大于C。


###输入描述:

输入第1行给出正整数T(<=10)，是测试用例的个数。随后给出T组测试用例，每组占一行，顺序给出A、B和C。整数间以空格分隔。



###输出描述:

对每组测试用例，在一行中输出“Case #X: true”如果A+B>C，否则输出“Case #X: false”，其中X是测试用例的编号（从1开始）。


###输入例子:

    4

    1 2 3

    2 3 4

    2147483647 0 2147483646

    0 -2147483648 -2147483647


输出例子:

    Case #1: false

    Case #2: true

    Case #3: true

    Case #4: false
	


    import java.util.Scanner;

    public class Main {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);//声明Scanner，并创建一个实例sc
            int t = sc.nextInt();// 测试用例个数T
            if (t <= 10) {// 判断T
                int i = 0;
                long a, b, c;

                while (i++ < t) {
                    a = sc.nextLong();
                    b = sc.nextLong();
                    c = sc.nextLong();
                    if ((a + b) > c) {
                        System.out.println("Case #" + i + ":" + " true");
                    } else {
                        System.out.println("Case #" + i + ":" + " false");
                    }
                }
            }
        }
    }
