C

用户需求原则：
如果有人跟你这么讲，我给你编了个程序，用的时候又这么麻烦，我估计你也就没有兴趣了，是吧。
希望即使是一个简单的功能，别人用得舒服点。
编得通用一点。

实际操作：
在运行的时候，把要算的原始数据给它，这样一运行
还提供了一个输入函数

知识点：
scanf("%d%d,&value1,&value2")  两个%d，说明要读两个整数进去，
第一个数给了value1，第二个数给了value2

动作及问题：
执行到scanf函数会自动停下来
算阶乘的，语言没有提供，编一个

笑话：我给你编了个程序，这个程序只能算15+12，假如你想算别的数，怎么办？我教你怎么改程序，把程序改一改，然后你再去运行，它就能算。

================================格式控制、数据类型、常量&变量==================================================================================
处理可多可少
%d 表示这个位置上输出一个10进制的整数，所以叫格式控制
下来还有 %f ，%c 但并不是所有的，如 %a 就没有意义

格式控制主要说明把什么样的数放在这里，但是不管什么样的数，
肯定是一个10进制的数	
%d 表示我把什么样的数放在这里，格式控制决定了什么样的输出格式
什么样子，已经规定了，具体的什么数值，看后面的参数

原样输出，%d 代表的参数表示会放一个数在这里
scanf 
需要分析的仍然是格式控制
对比：要求输出（入）一个什么样的数，
普通字符：要求原样输入什么样的数

什么意思呢？就是在输入的时候还要再打一遍

scanf("%d%d",&m,&n) 中间没有任何字符，但输入的时候是必须加的，不可能不加
& 是取地址符号

scanf("%d,%d") 输入的时候，“,”照打，起到了分隔符的作用
可以加个空格，加个“,”号

最好直接了当
不要的东西都不要加
每次都得打一遍
尤其不加 \n

编译，因为不是可执行程序，双击之不会动的

处理什么样的数据，实际问题能用基本的数据类型来表示，就能处理
构造数据类型：数组、结构、联合、枚举
指针 空类型

怎么操作 运算符，和运算对象组织在一起，就成了表达式
对一个语言来说，有一个量，怎么描述，就是常量和变量

常量就是具体的数值，在运行过程中不会改变的
运行多少遍，怎么运行都不用管
常量，原本提供了一套数据类型，也有数据类型，由书写格式所决定的 4.56 'A'

除了数，也可以是常量
可以定义PI，可以用标识符来表示一个常量的数据
PI表示什么，全看定义
这里区分用大写

# define PI 3.14
容易读，容易维护

前面讲的都是常量，现在讲变量
值是可以改变的，存放数据的单元


==============================================================讲了整型变量===================================



内存中的一个存储单元
定义一个、多个
见名知义
根据变量的类型来定义

变量名：要用之，取个名
对应1块存储单元，存其值

整数：2个字节
大小
指定了大小，名字，反映了一个存储单元

定义了就用
定义一次，放在函数最前面
语法要求前面，不是运行次序

使用：赋值
先赋值，再引用 不是语法要求
得到不能预料的结果

输入也是一种赋值
scanf
定义时对之赋初值，是新的方法
变量定义只有一次的，简单再改不要加类型

整型常量
首位是0代表8进制
16进制：a-f 加“0x”或“0X”
语法上都对

存储最后都是2进制

有限的
两个字节
最小： -32768 32767

%o %x
多了2个，8进、16进

格式控制，放进去时都是2进制
输出也是3种，怎么来让人看，格式符
输出不会引起误解，不再加0或0x

输入也可以是两种形式
scanf("%o%d",&a,&b)  17
如果赋值，把17看成8进，以格式符为准
后面的你打了0，也不认为是8进
输入输出是以格式符为准的

写常量的时候是以书写格式为准
%d 输出的宽度，给你了5个，对齐时用的
如果写1d，不会影响输出的，连输出都不对了

