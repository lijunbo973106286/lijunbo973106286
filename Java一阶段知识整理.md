# Java介绍

## 相关简介

#### 1.java介绍

Java是一门面向对象编程语言，不仅吸收了C++语言的各种优点，还摒弃了C++里难以理解的多继承、指针等概念，
	因此Java语言具有功能强大和简单易用两个特征。Java语言作为静态面向对象编程语言的代表，极好地实现了面向对象理论，
	允许程序员以优雅的思维方式进行复杂的编程
	

##### Java平台：

​		J2ME（Java2 Micro Edition，Java2平台的微型版），应用于移动、无线及有限资源的环境
​		J2SE（Java 2 Standard Edition，Java 2平台的标准版），应用于桌面环境，第一阶段内容，就是Java基础语法
​		*J2EE（Java 2Enterprise Edition，Java 2平台的企业版），应用于基于Java的应用服务器，是13种技术的统称

#### 3.Java语言的跨平台

​	什么是Java语言的跨平台？
​		就是指通过Java语言写好的程序，可以在任何操作系统上运行
​		注意： Java语言之所以能够跨平台是依赖于Java虚拟机(JVM)的，Java虚拟机本身也是不可以		跨平台的，但是针对不同的操作系统有不同的版本的Java虚拟机

#### 5.JDK,JRE和JVM？

​	什么是JDK？
​		Java的开发环境，软件，里面包含了开发工具包和JRE
​	什么是JRE？
​		Java的运行环境，里面包含了JVM和核心类库

​	什么是JVM？
​		Java虚拟机

​	三者之间的包含关系？
​		JDK > JRE > JVM

#### 6.环境变量的配置

为什么要配置环境变量？
		目的是为了在任意目录下可以使用javac.exe(编译)和java.exe(运行)
	怎么配置环境变量？

​	方式一：
​		1.此电脑，属性，找到高级系统设置
​		2.找到环境变量，打开
​		3.在系统变量中，找到path变量
​		4.将javac和java所在的目录(D:\develop\jdk1.8\jdk1.8.0_241\bin)添加到path变量中
​			path = D:\develop\jdk1.8\jdk1.8.0_241\bin	

​	方式二：
​			1.此电脑，属性，找到高级系统设置
​			2.找到环境变量，打开
​			3.在系统变量中，新建一个变量，名字叫做JAVA_HOME,值为javac和java所在目录，并且去			掉bin
​				JAVA_HOME = D:\develop\jdk1.8\jdk1.8.0_241
​			4.将JAVA_HOME添加到path变量中
​				path = %JAVA_HOME%\bin
​				

​		注意：
​			1.%%之间存放的是系统变量名
​			2.值与值之间用分号隔开

## JAVA相关基础知识

#### 	1.注释

​		什么是注释？
​		用来解释说明的，给我们程序员看的
​	
​		注释的分类？
​			*1.单行注释
​			//注释的内容
​		
​		*2.多行注释
​			/*注释的内容*/
​	
​		3.文档注释
​			/**注释的内容*/
​		
​	注释的作用？
​	1.用来解释说明的，提高了代码的阅读性
​	2.可以帮我们找到一些简单的错误bug
​	
​	注释的注意事项？
​	单行注释可以嵌套
​		// //约吗
​		
​	多行注释不可以嵌套
​		/*
​			约吗
​			/*
​				滚犊子
​			*/
​		*/

#### 3.关键字

​	什么是关键字？
​		关键字就是Java语言给我们提供好的一些单词，
​		每个单词都具有他自己的意义
​		

​	关键字的注意事项？
​		1.关键字的每个字母都是小写的
​		2.main不是关键字

#### 4.标识符

​		什么是标识符？
​			标识符就是我们自己起的名字
​		

​		标识符的组成规则？
​			由26个大小写英文字母，数字，美元符号$和下划线_组成
​			汉字...
​	
​		标识符的注意事项？
​			1.数字不能开头
​				2.标识符不能和关键字同名

#### 5.常量

​	什么是常量：常量就是永恒不变的量，分为字面值常量和自定义常量两大类

​		常量的分类？
​	字面值常量：
​		整数常量：
​			1,2,3,100,200.....
​		
​		小数常量：
​			3.14, 1.2, 1.3....
​		
​		字符常量：
​			'a', 'b', '约', '#', '1', ' '
​			
​			'约吗', ''
​			
​			注意：
​				1.字符常量必须由单引号括起来
​				2.字符常量里面有且只能有一个字符
​		
​		字符串常量：
​			"a", "ab", "约吗", "123", "#4$", ""
​		
​			注意：
​				字符串常量必须由双引号括起来
​		
​		布尔常量：
​			只有两个常量值
​			true
​			false
​			
​		空常量：
​			只有一个常量值
​			null
​		
​	自定义常量(即被final所修饰的变量就是自定义常量）

#### 6.进制

注：计算机底层的计算都是将十进制转变为二进制的补码进行计算，将结果转变为二进制原码再转变为十进制输出

​	生活中使用的是十进制
​	计算机中使用的是二进制
​	8位为一个字节

Java的进制分类？
	十进制：逢十进一,正常写
		10
		56
	

	二进制：逢二进一, 0b
		10010
		01001
		
		0b10010
		0b01001
	
	八进制：逢八进一, 0
		10
		
		032
	
	十六进制：逢十六进一, 0x
		0~9
		10：A
		11：B
		12：C
		13：D
		14：E
		15：F
		
		0x10
		0x43BC

在计算机中，所有的数据最终都会转变成二进制，也就是1和0组成，每一个1或者0都称为1个位(bit),8个bit组成1个byte
计算机对数据进行存储和运算的最小单位是字节(byte)，不是bit

​	8bit = 1byte
​	1KB = 1024byte
​	1MB = 1024KB
​	1GB = 1024MB
​	1TB = 1024GB

进制的转换？
	8421码进制转换法

​	详情参考图片**

#### 7.原码，反码和补码

​	计算机对数据进行运算的原理：
​		3 + 2 = 5
​		

​	计算机底层会将3这个十进制转变成二进制的原码形式，然后变成反码形式，最后变成补码形式
​				将2这个十进制转变成二进制的原码形式，然后变成反码形式，最后变成补码形式
​				将3的补码和2的补码相加，得到一个补码，
​				将这个结果的补码变成反码，再变成原码，最终转换成十进制，就是5
​		
​	正数：原码反码补码转换
​		原码，反码和补码是一样的
​	
​	负数：原码反码补码转换
​		原码 -> 反码：除去符号位，其余1变0,0变1
​		反码 -> 补码：+1
​		
​	符号位：最左边的那一位就是符号位，正数的符号位是0，负数的符号位是1

#### 8.变量

​	什么是变量？
​		在一定范围内，可以变化的量
​		

变量的定义格式？
	格式一：数据类型 变量名 = 数据;(直接定义)
			  int      i    =   12;
	
	格式二：数据类型 变量名;
			 变量名 = 数据;(间接定义)
			 
			 int  a;
			 a = 13;

说明：当我们运行这句话(int i = 12)的时候，在内存中会开辟一块内存空间，该空间的名字就是我们自己起的i，
该空间中存储的数据的数据类型就是我们自己定义的int类型，该空间中存储的数据就是我们给的12。

#### 9.数据类型

​	Java中数据类型的分类？
​		2大类4小类8小种
​		

​	基本数据类型：
​		4小类8小种
​		整型：
​			byte(1个字节)   范围（-2^7到2^7-1）即（-128到127）
​			short(2个字节)	范围（-2^15到2^15-1）
​			int(4个字节)	范围（-2^31到2^31-1）
​			long(8个字节)	范围（-2^63到2^63-1）
​			
​		浮点型：
​			float(4个字节)
​			double(8个字节)
​			
​		字符型：
​			char(2个字节)
​		
​		布尔型：
​			boolean(1个字节)
​		
​	引用数据类型(String 数组 枚举 自定义的类等等)

#### 10.数据类型的转换

​	隐式类型转换？
​		什么是隐式类型转换？
​			是指小的数据类型会自动提升为大的数据类型
​			

​	举例子：
​		byte b = 1;
​		short s = 2;
​		int i = 3;
​		long l = 4;
​		float f = 5.5F;
​		double d = 6.6;
​		double dd = b + s + i + l + f + d;
​		System.out.println(dd);
​		
​		注意：当有多个数据类型参与运算的时候，小的数据类型会提升为大的数据类型
​		
​	常见的考试题？
​		考一：
​			byte b1 = 1;
​			byte b2 = 2;
​			byte b3 = b1 + b2;
​			System.out.println(b3);//编译报错
​			

---------------------------------

​			short s1 = 1;
​			short s2 = 2;
​			short s3 = s1 + s2;
​			System.out.println(s3);//编译报错
​			
---------------------------------

​			int i1 = 1;
​			int i2 = 2;
​			int i3 = i1 + i2;
​			System.out.println(i3);//3（因为默认为int，所以int及以上都可以）
​			
​		考二：
​			byte b1 = 1;
​			byte b2 = b1 + 2;
​			System.out.println(b2);//编译报错
​			
​		考三：
​			byte b = 126 + 1;
​			System.out.println(b);//127
​			
​		考四：
​			byte b = 127 + 1;
​			System.out.println(b);//编译报错

强制类型转换？
	什么是强制类型转换？
		是指大的数据类型强制转换为小的数据类型
		
	强制类型转换的格式？
		小的数据类型 小的数据类型变量名 = (小的数据类型)大的数据类型变量名
		
		例子：
			int i = 12;
			byte b = i;
			System.out.println(b); //错误写法

---------------------------------

​			int i = 12;
​			byte b = (byte)i;
​			System.out.println(b);
​			
​	注意事项？
​		我们能不使用强转尽量不要使用强转
​		
​		int i = 130;
​		byte b = (byte)i;
​		System.out.println(b);//-126

注意：boolean类型是不可以和其他的数据类型相互转换的

#### 11.ASCII编码表：

​		暂时简单记几个：'a' -> 97
​							'A' -> 65
​							'0' -> 48

#### 12.运算符

##### 	算术运算符：

​		+：
​			三个含义：
​				1.四则运算的+号
​				2.正负的正号
​				*3.连接符
​					任何数据类型的数据与字符串相加，加号都作为连接符
​		-
​		*
​		/：
​			**整数除以整数，得到的结果也是整数**
​			

​	%：模，取余
​		
​	++：
​		单独使用：
​			int i = 1;
​			i++; // i = i + 1
​			System.out.println(i);//2
​			

-----------------------------

​			int i = 1;
​			++i;
​			System.out.println(i);//2
​			
​			注意：++不管在前，还是在后，对结果来说都没有影响
​		
​		参与运算：
​			++在前：先自身加1，然后再参与运算
​				int i = 1;
​				System.out.println(++i);
​				

---------------------------

​				int i = 1;
​				int j = ++i;
​				System.out.println(i);
​				System.out.println(j);
​			
​			++在后：先参与运算，然后再自身加1
​				int i = 1;
​				System.out.println(i++);
​				
---------------------------

​				int i = 1;
​				int j = i++;
​				System.out.println(i);
​				System.out.println(j);
​			
​		面试题：
​			byte b = 1;
​			b = b + 1;
​			System.out.println(b);//编译报错
​			
----------------------

​			byte b = 1;
​			b++; // b = (byte)(b + 1)
​			System.out.println(b);//2
​			
​			自带强制类型转换
​	
​	--：
​		单独使用：
​			int i = 2;
​			i--;// i = i - 1
​			System.out.println(i);
​			
------------------------

​			int i = 2;
​			--i;// i = i - 1;
​			System.out.println(i);
​			
​			注意：--不管在前，还是在后，对结果来说都没有影响
​		
​		参与运算：
​			--在前：先自身减1，然后再参与运算
​				int i = 2;
​				System.out.println(--i);
​				
---------------------------

​				int i = 2;
​				int j = --i;
​				System.out.println(i);
​				System.out.println(j);
​			
​			--在后：先参与运算，然后再自身减1
​				int i = 2;
​				System.out.println(i--);
​				
---------------------------

​				int i = 2;
​				int j = i--;
​				System.out.println(i);
​				System.out.println(j);
​				
​	练习题：
​		int i = 5;
​		int j = i++ + ++i + --i + i--;
​		System.out.println(j);//24 

##### 赋值运算符：

​	=：
​		int i = 5;
​		
​	+=：
​		int i = 1;
​		i += 1;//i = i + 1
​		System.out.println(i);
​		

--------------------------

​		int i = 1;
​		i += 2;// i = i + 2
​		System.out.println(i);
​	
​	-=
​	*=
​	/=
​	%=
​	
​	注意：自带强制类型转换

##### 关系运算符(条件运算符)： 

​	关系运算符的结果一定是boolean类型的数据，要么是true，要么是false
​	
​	>
​	<
​	>=
​	<=
​	!=
​	==（当两边是数值的时候，比较的是否相等，当不为数值时，比较的是地址值）

##### 逻辑运算符：

​	逻辑运算符的两边都只能是boolean类型的数据，得到的结果也必须是boolean类型的数据
​	
​	&(单与)：
​		System.out.println(true & true);//true
​		System.out.println(true & false);//false
​		System.out.println(false & true);//false
​		System.out.println(false & false);//false
​		
​		*结论：只有两边都为true，结果才为true
​	
​	|(单或)：
​		System.out.println(true | true);//true
​		System.out.println(true | false);//true
​		System.out.println(false | true);//true
​		System.out.println(false | false);//false
​		
​		*结论：两边只要有一个为true，结果就为true
​		
​	^(异或)：
​		System.out.println(true ^ true);//false
​		System.out.println(true ^ false);//true
​		System.out.println(false ^ true);//true
​		System.out.println(false ^ false);//false
​		
​		结论：两边相同，为false，两边不同，为true
​	
​	!(非)：
​		System.out.println(true);//true
​		System.out.println(!true);//false
​		System.out.println(!!true);//true
​		System.out.println(!!!true);//false
​	
​	&&(双与)：
​		System.out.println(true && true);//true
​		System.out.println(true && false);//false
​		System.out.println(false && true);//false
​		System.out.println(false && false);//false
​		
​		*结论：只有两边都为true，结果才为true
​	
​	||(双或)：
​		System.out.println(true || true);//true
​		System.out.println(true || false);//true
​		System.out.println(false || true);//true
​		System.out.println(false || false);//false
​		
​		*结论：两边只要有一个为true，结果就为true
​		
​	面试题？
​		&和&&的区别？
​			&：如果左边为false，右边依然要继续执行，结果一定为false
​			&&：如果左边为false，右边就不再执行，结果一定为false
​		
​		|和||的区别？
​			|：如果左边为true，右边依然要继续执行，结果一定为true
​			||：如果左边为true，右边就不再执行，结果一定为true
​			
​		推荐使用&&和||，提高了效率

##### 位运算符：

​	位运算符的两边都只能是数值，得到的结果也必须是数值
​	
​	&(与位运算)：
​		3 & 2 = 2
​	
​	|(或位运算)：
​		3 | 2 = 3
​		
​	^(异或位运算)：
​		3 ^ 2 = 1
​		
​		练习题？
​			已知：int i = 1, int j = 2，通过某些方式来实现两个变量的数据的交换？
​				方式一：
​					使用第三个变量
​	
​					int i = 1;
​					int j = 2;
​					int a = i;
​					i = j;
​					j = a;
​					System.out.println(i + "..." + j);
​				
​				方式二：
​					使用异或位运算
​					
​					int i = 1;
​					int j = 2;
​					i = i ^ j;
​					j = i ^ j;
​					i = i ^ j;
​					System.out.println(i + "..." + j);
​					
​	~(按位取反)：
​		System.out.println(~3);
​		
​		注意：符号位也要取反
​	
​	>>(右移)：
​		3 >> 2 = 0
​		
​		公式： A >> B --> A / 2^B
​		
​		面试题？
​			如何实现最快速的得到4/2=2的结果？
​			
​			4/2 = 2
​			4 >> 1 = 2 效率快，因为这种写法直接操作的是二进制
​	
​	<<(左移)：
​		3 << 2 = 12
​		
​		公式：A << B --> A * 2^B
​	
​	>>>(无符号右移)：
​		不管符号位是1还是0，右移之后，一律都补0

##### 三元运算符(三目运算符)：

​		**注意：三元运算符的结果是一个值，需要用对应的变量来接收（treemap集合中的比较器用的比较多）**

​		格式：
​			条件表达式 ? 表达式1 : 表达式2;
​			

​	执行流程：
​		会先判断条件表达式的结果，如果结果为true，会执行表达式1，不会执行表达式2
​								  如果结果为false，会执行表达式2，不会执行表达式1
​		
​	例子：
​		int a = true ? 1 : 2;
​		System.out.println(a);
​		

---------------------

​		需求：判断两个数的大小，将大的数打印出来
​			int a = 12;
​			int b = 13;
​			
​			int max = a > b ? a : b;
​			System.out.println(max);
​			
​	注意事项？
​		1.三元运算符既然是一个运算符，就一定会得到一个结果，所以呢，我们要么将该结果赋值给一个变量，
​		要么将该结果在输出语句中输出
​			int a = 1 > 3 ? 1 : 3;
​			System.out.println(a);
​			
-------------------------------------

​			System.out.println(1 > 3 ? 1 : 3);
​			
​		2.当我们将三元运算符的结果赋值给一个变量的时候，变量的数据类型一定要和结果的类型匹配

#### 13.键盘录入

​	实现键盘录入的步骤？
​		第一步：导包
​			import java.util.Scanner;
​			

​		放在class的上面
​	
​	第二步：创建对象
​		Scanner sc = new Scanner(System.in);
​	
​	第三步：调用方法
​		int num = sc.nextInt();
​		System.out.println(num);
​	
​		String s = sc.next();
​		System.out.println(s);

## 各种语句（条件、循环等语句）

#### 1.if语句

​	格式一：
​		if(条件表达式) {
​			语句体内容;
​		}
​	

​	执行流程：
​		当程序执行到if语句时候，会先看条件表达式的结果是true还是false，
​		如果为true，则进入到if语句体中，执行语句体内容
​		如果为false，则不会进入到if语句体中，就不会执行到语句体内容
​	
​	例子：
​		if(3 > 2) {
​			System.out.println("约吗");
​		}
​		
​		System.out.println("滚犊子");
​		
​	常见的考试题：
​		考一：
​			boolean b = true;
​			if(b == false) {
​				System.out.println("在吗");
​			}
​			System.out.println("约吗");
​			
​		考二：
​			boolean b = true;
​			if(b = false) {
​				System.out.println("在吗");
​			}
​			System.out.println("约吗");
​		
​		考三：
​			boolean b = true;
​			if(b);{
​				System.out.println("在吗");
​			}
​			System.out.println("约吗");
​			
​		考四：
​			boolean b = false;
​			if(b)
​				System.out.println("在吗");
​			System.out.println("约吗");
​			
​			注意：当if语句中的有效语句只有一条的时候，或者没有的时候，花括号可以省略不写
​			
​		考五：
​			boolean b = false;
​			if(b)
​				int i = 1;
​			System.out.println("约吗");//运行报错，int i=1在底层是两条语句
​	
格式二：
​	if(条件表达式) {
​		语句体内容;
​	} else {
​		语句体内容;
​	}
​	
​	执行流程：
​		当程序执行到if语句的时候，会先看if语句中的条件表达式的结果，
​		如果为true，就会进入到if语句中，执行if中的语句体内容，不会执行else中的语句体内容
​		如果为false，就不会进入到if语句中执行语句体内容，会进入到else中执行语句体内容

​	例子：
​		if(3 > 2) {
​			System.out.println("哈哈");
​		} else {
​			System.out.println("嘻嘻");
​		}

​	注意：
​		if语句的第二种格式是可以和三元运算符互换使用的
​		
​		if语句写法麻烦一些，但是可读性高一些
​		三元运算符写法简单一些，但是可读性差一些
​		
格式三：
​	if(条件表达式) {
​		语句体内容;
​	} else if(条件表达式) {
​		语句体内容;
​	} else if(条件表达式) {
​		语句体内容;
​	} ... ...
​	else {
​		语句体内容;
​	}
​	
​	执行流程：
​		当程序执行到if语句的时候，会先看if里的条件表达式是true还是false，
​		如果为true，直接进入到if中，执行里面的语句体内容
​		如果为false，程序继续向下执行，会看elseif中条件表达式是true还是false,
​		如果为true，进入到elseif中执行里面的语句体内容，
​		如果为false，程序继续向下执行
​		如果if和所有的elseif中的条件表达式都为false，就会进入到else中，执行里面的语句体内容
​		
​	例子：
​		int i = 4;
​		if(i > 4) {
​			System.out.println("哈哈");
​		} else if(i > 3) {
​			System.out.println("呵呵");
​		} else if(i > 2) {
​			System.out.println("嘻嘻");
​		} else {
​			System.out.println("嘿嘿");
​		}
​		
​	注意：
​		当else中没有语句体内容的时候，else是可以省略不写的
​		int i = 4;
​		if(i > 4) {
​			System.out.println("哈哈");
​		} else if(i > 3) {
​			System.out.println("呵呵");
​		} else if(i > 2) {
​			System.out.println("嘻嘻");
​		} else {
​			
​		}

--------------------------------------
​		int i = 4;
​		if(i > 4) {
​			System.out.println("哈哈");
​		} else if(i > 3) {
​			System.out.println("呵呵");
​		} else if(i > 2) {
​			System.out.println("嘻嘻");
​		}
​	
​	考试题？
​		int a;
​		int i = 4;
​		if(i > 5) {
​			a = 1;
​		} else if(i > 4) {
​			a = 2;
​		} else if(i > 3) {
​			a = 3;
​		} else if(i > 2) {
​			a = 4;
​		}
​		System.out.println(a);//编译报错(系统会判断有可能不能进入if语句体中，a可能会没有赋值，因此报错)

#### 2.switch语句

​	格式：
​		switch(表达式) {
​			case 取值1:
​				语句体内容;
​				break;
​			caes 取值2:
​				语句体内容;
​				break;
​			... ...
​			default:
​				语句体内容;
​				break;
​		}
​		

执行流程：
	当程序执行到switch语句的时候，就会拿表达式去和第一个case进行匹配，如果匹配成功，就会进入到case中，
	执行里面的语句体内容和break，switch语句结束，如果没有匹配，就继续向下执行，和其他的case继续匹配，
	如果所有的case都不匹配，最后会执行defautl中的语句体内容和break
	
例子：
	int a = 3;
	switch(a) {
		case 1:
			System.out.println("哈哈");
			break;
		case 2:
			System.out.println("呵呵");
			break;
		case 3:
			System.out.println("嘻嘻");
			break;
		case 4:
			System.out.println("嘿嘿");
			break;
		default:
			System.out.println("嘤嘤");
			break;
	}

我们在使用switch语句需要注意哪些问题？
	1.switch语句中的表达式数据的数据类型可以有哪些？
		byte
		short
		int
		char
		String
		枚举（enum）
		
	2.default可以放在任何一行，但是不管放到哪一行，都会优先去找case匹配，如果所有的case都不匹配，才会
	去找defautl
	  default中如果没有内容，default是可以省略不写的，但是建议写上
	  
	3.break关键字可以省略不写，但是如果不写break的话会造成switch穿透
		当匹配完一次case或者执行完一次default之后就不会再进行二次匹配了，但是内容该执行还是要执行的，直到遇到break关键字或者结尾“}”才会停止，这种现象就称为switch穿透。
	
	4.switch语句的结束标记？
		a.break
		b.}

什么时候用switch，什么时候用if？
	如果判断的是某个区间范围，建议使用if
	如果判断的是某几个数据，建议使用switch

#### 3.代码块的分类：

​		什么是代码块？

​				由一对花括号括起来的就称为代码块

​				{

​						}

1. 局部代码块：写在方法中的代码块就称为局部代码块，作用是可以让局部变量提前消失，节约内存
2. 构造代码块：写在类中，方法外的代码块就称为构造代码块。作用：由于它随着构造方法的每一次调用，就会出现一次（优先于构造方法），所以可以将这些方法的共性内容放在这个构造代码块中。
3. 静态代码块：构造代码块前面加一个"static"关键字。作用：由于存在在方法区，所以会随着类的加载而加载，且只加载一次，所以可以将那些只需加载一次，且不变的内容放在其中
4. 同步代码块：由synchronize修饰的代码块。 作用：用于解决线程安全问题。

#### 4.for循环

​	需求：在控制台上输出10个1？
​		System.out.println(1);
​		System.out.println(1);
​		System.out.println(1);
​		System.out.println(1);
​		System.out.println(1);
​		System.out.println(1);
​		System.out.println(1);
​		System.out.println(1);
​		System.out.println(1);
​		System.out.println(1);
​		

格式：
	for(初始化条件; 判断条件; 控制条件) {
		语句体内容;
	}
	
	初始化条件：一般写变量的定义， int i = 1
	判断条件：关系运算符，结果一定是boolean类型的数据
	控制条件：变量的自增，i++，i+=1
	语句体内容：需要重复执行的代码

执行流程：
	初始化条件 --> 判断条件 --> 语句体内容 --> 控制条件
			   --> 判断条件 --> 语句体内容 --> 控制条件
			   --> 判断条件 --> 语句体内容 --> 控制条件
			   ... ...
			   直到判断条件不满足的，循环结束
			   
练习：
	需求1：在控制台上输出10个1？
		for(int i = 1; i <= 10; i++) {
			System.out.println(1);
		}
		
	需求2：在控制台上打印出1-10的数字？
		for(int i = 1; i <= 10; i++) {
			System.out.println(i);
		}
		
	需求3：在控制台上打印出1-10的和？(累加和思想)
		int sum = 0; 
		for(int i = 1; i <= 10; i++) {
			sum = sum + i;
		}
		System.out.println(sum);
	
	需求4：在控制台上打印出1-100之间的所有偶数？
		方式一：
			for(int i = 1; i <= 100; i++) {
				//判断i是否为偶数
				if(i % 2 == 0) {
					System.out.println(i);
				}
			}
			
		方式二：
			for(int i = 1; i <= 100; i++) {
				//判断i是否为偶数
				if(i % 2 != 1) {
					System.out.println(i);
				}
			}
			
		方式三：
			for(int i = 2; i <= 100; i+=2) {
				System.out.println(i);
			}
	
	需求5：在控制台上打印出1-10之间的奇数的个数？(统计思想)
		int count = 0; //计数器
		for(int i = 1; i <= 10; i++) {
			//判断i是否为奇数
			if(i % 2 == 1) {
				count++;
			}
		}
		System.out.println(count);

#### 5.while循环（死循环有时比较常用）

​	格式：
​		初始化条件;
​		while(判断条件) {
​			语句体内容;
​			控制条件;
​		}
​	

执行流程：
	初始化条件 --> 判断条件 --> 语句体内容 --> 控制条件
			   --> 判断条件 --> 语句体内容 --> 控制条件
			   --> 判断条件 --> 语句体内容 --> 控制条件
			   ... ...
			   直到判断条件不满足的，循环结束

练习：
	需求1：在控制台上输出10个1？
		int i = 1;
		while(i <= 10) {
			System.out.println(1);
			i++;
		}
		
	需求2：在控制台上打印出1-10的数字？
		int i = 1;
		while(i <= 10) {
			System.out.println(i);
			i++;
		}
		
	需求3：在控制台上打印出1-10的和？(累加和思想)
		int sum = 0;
		int i = 1;
		while(i <= 10) {
			sum += i;
			i++;
		}
		System.out.println(sum);
	
	需求4：在控制台上打印出1-100之间的所有偶数？
		int i = 1;
		while(i <= 100) {
			if(i % 2 == 0) {
				System.out.println(i);
			}
			i++;
		}
	
	需求5：在控制台上打印出1-10之间的奇数的个数？(统计思想)
		int count = 0;
		int i = 1;
		while(i <= 10) {
			if(i % 2 == 1) {
				count++;
			}
			i++;
		}
		System.out.println(count);

#### 6.do...while循环（不常用）

​	格式：
​		初始化条件
​		do {
​			语句体内容;
​			控制条件
​		} while(判断条件);
​	

执行流程：
	初始化条件 --> 语句体内容 --> 控制条件 --> 判断条件
				   语句体内容 --> 控制条件 --> 判断条件
				   语句体内容 --> 控制条件 --> 判断条件
				   ... ...
				   语句体内容 --> 控制条件 --> 判断条件不满足的时候，循环结束

练习：
	需求：在控制台上打印出1-10的数字？
		int i = 1;
		do {
			System.out.println(i);
			i++;
		} while(i <= 10);

#### 7.三个循环的区别（for循环、while循环、do...while循环）

for,while和do...while？
		对于for,while来说，语句体内容和控制条件可以一次都不执行，判断条件永远都比控制条件和语句体内容多执行一次
		对于do...while来说，语句体内容和控制条件至少会执行一次，判断条件和语句体内容和控制条件执行的次数一样多
		

for和while？
	对于for来说，初始化条件出了for循环就在内存中消失了
		for(int i = 1; i <= 10; i++) {

​		}
​		
​		System.out.println(i);//编译报错，因为找不到i变量
​		
​		变形写法：
​		int i;
​		for(i = 1; i <= 10; i++) {
​		
​		}
​		System.out.println(i);
​	
​	对于while来说，初始化条件和while结构体本身就没有关系，出了while训话，照样可以使用
​		int i = 1;
​		while(i <= 10) {
​			i++;
​		}
​		
​		System.out.println(i);
​		
​	什么时候使用for什么时候使用while？
​		明确循环次数建议使用for
​		不明确循环次数建议使用while

#### 8.break和continue关键字

​	*break关键字：
​		1.用来switch语句中，作为switch语句结束标记
​		2.用来循环中，作为循环的结束标记(结束整个循环)
​		

continue关键字：
	1.用来循环中，作为循环的结束标记(结束本次循环，还会继续下一次循环的)

注意事项？
	for(int i = 1; i <= 10; i++) {
		if(i == 3) {
			break;
			System.out.println(i);
		}
		
		System.out.println(i);
	}

---------------------------------

​	for(int i = 1; i <= 10; i++) {
​		if(i == 3) {
​			continue;
​			System.out.println(i);
​		}
​		
​		System.out.println(i);
​	}
​	
​	在同一对花括号内，break和continue下面不能有任何语句，因为永远都执行不到

#### 9.死循环

​	永远出不来的循环
​		

for的死循环：
	for(;;) {
	
	} 

*while的死循环：
	while(true) {
	
	}

#### 10.循环的嵌套

​	什么是循环的嵌套？
​		循环中还有循环
​		

需求：在控制台上打印出由*组成的矩形？

​	方式一：
​		public class Demo05 {
​			public static void main(String[] args) {
​				System.out.println("*****");
​				System.out.println("*****");
​				System.out.println("*****");
​				System.out.println("*****");
​			}
​		}
​	
​	方式二：
​		public class Demo05 {
​			public static void main(String[] args) {
​				for(int i = 1; i <= 4; i++) {
​					System.out.println("*****");
​				}
​			}
​		}
​		
​	方式三：
​		for(int i = 1; i <= 4; i++) {
​			for(int j = 1; j <= 5; j++) {
​				System.out.print("*");
​			}
​			System.out.println();//换行
​		}
​	
​	结论：外层循环控制的行数，内层循环控制列数
​	
需求：在控制台上打印出由*组成的直角三角形？
​	*
​	**

方式一：
		public class Demo06 {
			public static void main(String[] args) {
				System.out.println("*");
				System.out.println("**");
				System.out.println("***");
				System.out.println("** **");
				System.out.println("** ***");
			
		}
		
	方式二：
		for(int i = 1; i <= 5; i++) {
			//外层循环第一次，内层循环1次
			//外层循环第二次，内层循环2次
			for(int j = 1; j <= i; j++) {
				System.out.print("*");
			}
			System.out.println();//换行
		}

## 数组

#### 1.数组

什么是数组？
		就是一个容器（数组，集合）
	

数组的作用是什么？
	装东西，装数据，方便对数据进行管理和操作的
	
数组容器的特点是什么？
	1.数组容器一旦初始化，长度就固定了，不可以再改变（集合长度可变）
	2.数组容器里面既可以存储基本数据类型，也可以存储引用数据类型
	3.一个数组容器中存储的所有的数据的数据类型必须一致（集合可以为各种类型）
	
数组的定义格式？
	格式一：
		数据类型[] 数组名 = new 数据类型[数组的长度];
		
		  int[]	    arr   = new int[3];
		  int		arr[] = new int[3];
	
	格式二：
		数据类型[] 数组名 = new 数据类型[]{元素1,元素2, ......};
		
		   int[]    arr   = new int[]{12,13,14};
	
	格式三：
		数据类型[] 数组名 = {元素1,元素2, ......};
		   int[]    arr   = {12,13,14};

数组容器的使用？
	1.创建数组容器
		int[] arr = new int[3];
	
	2.向数组容器中装东西（数组的长度： 数组名.length）
		格式：数组名[索引] = 东西;
		
		索引：编号的意思，编号是从0开始
		
		arr[0] = 12;
		arr[1] = 13;
		arr[2] = 14;
	
	3.从数组容器中取东西
		格式：数组名[索引]
		
		int a = arr[0];
		int b = arr[1];
		int c = arr[2];
		System.out.println(a);
		System.out.println(b);
		System.out.println(c);

-------------------------

​		System.out.println(arr[0]);
​		System.out.println(arr[1]);
​		System.out.println(arr[2]);
​		
数组的内存图？
​	Java中内存有几块？
​		*栈
​		*堆
​		*方法区
​		本地方法栈
​		寄存器
​		
​	1.一个数组的内存图？
​		int[] arr = new int[3];
​		
​		System.out.println(arr);
​		System.out.println(arr[0]);
​		System.out.println(arr[1]);
​		System.out.println(arr[2]);
​		
​		arr[0] = 12;
​		arr[1] = 13;
​		
​		System.out.println(arr[0]);
​		System.out.println(arr[1]);
​		System.out.println(arr[2]);
​		
​		详情参考画图
​		
​	2.二个数组的内存图？
​		int[] arr1 = new int[]{12,13,14};
​		
​		System.out.println(arr1);
​		System.out.println(arr1[0]);
​		System.out.println(arr1[1]);
​		System.out.println(arr1[2]);
​		
​		arr1[2] = 15;
​		
​		System.out.println(arr1[0]);
​		System.out.println(arr1[1]);
​		System.out.println(arr1[2]);
​		
​		int[] arr2 = {3,4};
​		
​		System.out.println(arr2);
​		System.out.println(arr2[0]);
​		System.out.println(arr2[1]);
​		
​		arr2[1] = 5;
​		
​		System.out.println(arr2[0]);
​		System.out.println(arr2[1]);
​	
​		详情参考画图
​		
​	3.一个变量(引用)指向两个数组容器的内存图？
​		int[] arr = new int[2];
​		
​		System.out.println(arr);
​		System.out.println(arr[0]);
​		System.out.println(arr[1]);

​		arr[1] = 12;
​		
​		System.out.println(arr[0]);
​		System.out.println(arr[1]);
​		
​		arr = new int[3];
​		
​		System.out.println(arr);
​		System.out.println(arr[0]);
​		System.out.println(arr[1]);
​		
​		arr[0] = 13;
​		
​		System.out.println(arr[0]);
​		System.out.println(arr[1]);
​		System.out.println(arr[2]);
​	
​		详情参考画图
​		
​	4.两个变量(引用)指向了一个数组容器？
​		int[] arr1 = new int[2];
​		
​		System.out.println(arr1);
​		System.out.println(arr1[0]);
​		System.out.println(arr1[1]);
​		
​		arr1[0] = 12;
​		arr1[1] = 13;
​	
​		int[] arr2 = arr1;
​		
​		System.out.println(arr2);
​		System.out.println(arr2[0]);
​		System.out.println(arr2[1]);
​		
​		arr2[0] = 15;
​		arr2[1] = 16;
​		
​		System.out.println(arr2[0]);
​		System.out.println(arr2[1]);
​		
​		System.out.println(arr1[0]);
​		System.out.println(arr1[1]);
​		
​		详情参考画图
​		
我们在使用数组的时候遇到最常见的两个异常？
​	1.数组索引越界异常(ArrayIndexOutOfBoundsException)
​	
​		int[] arr = new int[3];
​		
​		System.out.println(arr);
​		System.out.println(arr[0]);
​		System.out.println(arr[1]);
​		System.out.println(arr[2]);
​		System.out.println(arr[3]);//报错
​		
​	2.空指针异常(NullPointerException)
​		int[] arr = {1,2};
​		
​		System.out.println(arr);
​		System.out.println(arr[0]);
​		System.out.println(arr[1]);
​		
​		arr = null;
​		
​		System.out.println(arr);
​		System.out.println(arr[0]);
​		System.out.println(arr[1]);
​		
​		注意：null空常量只能给引用数据类型的变量赋值
​			int[] arr = null;
​			String s = null;
​			
数组的常见操作？

##### 	1.遍历

​		什么是遍历？
​			就是将数组容器中的数据挨个获取到
​			
​		int[] arr = {1,2,3,4,5};
​		
​		System.out.println(arr[0]);
​		System.out.println(arr[1]);
​		System.out.println(arr[2]);
​		System.out.println(arr[3]);
​		System.out.println(arr[4]);
​		

-----------------------------

​		for(int i = 0; i <= 4; i++) {
​			System.out.println(arr[i]);
​		}
​		
-----------------------------

​		获取数组容器的长度：数组名.length
​		  arr.length
​							  
​		数组的最小索引：0
​		数组的最大索引：arr.length - 1
​		
​		/*for(int i = 0; i < arr.length; i++) {
​			System.out.println(arr[i]);
​		}*/
​		
​		for(int i = 0; i <= arr.length - 1; i++) {
​			System.out.println(arr[i]);
​		}
​	

##### 	2.获取最值

​		最大值，最小值
​		
​		需求：已知有一个数组，获取数组容器元素最大的值？
​			int[] arr = {1,4,3,6,2,5};
​			
​			方式一：
​				int[] arr = {1,4,3,6,2,5};
​	
​				int max = arr[0];
​				
​				for(int i = 1; i <= arr.length - 1; i++) {
​					if(max < arr[i]) {
​						max = arr[i];
​					}
​				}
​				
​				System.out.println(max);
​				
​			方式二：
​				int max = 0;
​	
​				for(int i = 1; i < arr.length; i++) {
​					if(arr[max] < arr[i]) {
​						max = i;
​					}
​				}
​				
​				System.out.println(arr[max]);
​	

##### 	3.基本查找

​		需求：已知有一个数组容器，我们键盘录入一个数，判断该数在容器中是否存在，存在打印对应的元素索引，
​		不存在打印-1？
​		
​			//创建容器
​			int[] arr = {1,2,3,4,5,6,7,8,9,10};
​			
​			//创建对象
​			Scanner sc = new Scanner(System.in);
​			System.out.println("请输入一个要查找数字：");
​			//调用方法
​			int num = sc.nextInt();
​			
​			//定义一个索引变量
​			int index = -1;
​			
​			//遍历容器
​			for (int i = 0; i < arr.length; i++) {
​				if(arr[i] == num) {
​					index = i;
​					break;
​				}
​			}
​			
​			System.out.println(index);

##### 4.反转

​			反转前：arr -> {1,2,3,4,5}
​			反转后：arr -> {5,4,3,2,1}
​			

​		方式一：
​			//创建数组容器
​			int[] arr = {1,2,3,4,5};
​			
​			//遍历
​			for (int i = 0; i < arr.length; i++) {
​				System.out.print(arr[i] + " ");
​			}
​			System.out.println();//换行
​			
​			//反转
​			for(int i = 0; i < arr.length / 2; i++) {
​				int temp = arr[i];
​				arr[i] = arr[arr.length - 1 - i];
​				arr[arr.length - 1 - i] = temp;
​			}
​			
​			//遍历
​			for (int i = 0; i < arr.length; i++) {
​				System.out.print(arr[i] + " ");
​			}
​			System.out.println();//换行
​		
​		方式二：
​			//创建数组容器
​			int[] arr = {1,2,3,4,5};
​			
​			//遍历
​			for (int i = 0; i < arr.length; i++) {
​				System.out.print(arr[i] + " ");
​			}
​			System.out.println();//换行
​			
​			//反转
​			for(int i = 0,j = arr.length - 1; i < arr.length / 2; i++, j--) {
​				int temp = arr[i];
​				arr[i] = arr[j];
​				arr[j] = temp;
​			}
​			
​			//遍历
​			for (int i = 0; i < arr.length; i++) {
​				System.out.print(arr[i] + " ");
​			}
​			System.out.println();//换行
​		

##### 	5.排序

​		排序前：arr -> {3,5,1,4,2}
​		排序后：arr -> {1,2,3,4,5}
​		
​		方式一：选择排序
​			int[] arr = {3,5,1,4,2};
​	
​			//遍历
​			for (int i = 0; i < arr.length; i++) {
​				System.out.print(arr[i] + " ");
​			}
​			System.out.println();//换行
​			
​			//排序
​			for(int i = 0; i < arr.length - 1; i++) {
​				for(int j = i + 1; j < arr.length; j++) {
​					if(arr[i] > arr[j]) {
​						int temp = arr[i];
​						arr[i] = arr[j];
​						arr[j] = temp;
​					}
​				}
​			}
​			
​			//遍历
​			for (int i = 0; i < arr.length; i++) {
​				System.out.print(arr[i] + " ");
​			}
​			System.out.println();//换行
​		
​		*方式二：冒泡排序
​			int[] arr = {3,5,1,4,2};
​	
​			//遍历
​			for (int i = 0; i < arr.length; i++) {
​				System.out.print(arr[i] + " ");
​			}
​			System.out.println();//换行
​			
​			//排序
​			for(int i = 0; i < arr.length - 1; i++) {
​				for(int j = 0; j < arr.length - 1 - i; j++) {
​					if(arr[j] > arr[j + 1]) {
​						int temp = arr[j];
​						arr[j] = arr[j + 1];
​						arr[j + 1] = temp;
​					}
​				}
​			}
​			
​			//遍历
​			for (int i = 0; i < arr.length; i++) {
​				System.out.print(arr[i] + " ");
​			}
​			System.out.println();//换行

#### 2.二维数组

​	什么是二维数组？
​		元素是一维数组的数组
​		

二维数组的定义格式？
	格式一：
		数据类型[][] 数组的名字 = new 数据类型[二维数组的长度] [一维数组的长度];
		
		    int[] []      arr    = new    int[3] [2];
			
			3是什么意思？
				arr中存放了3个一维数组
			2是什么意思？
				每一个一维数组中存放了2个元素
	
	格式二：
		数据类型[][] 数组的名字 = new 数据类型[二维数组的长度] [];
		
			int[][]     arr     = new    int[3] [];
	
			3是什么意思？
				arr中存放了3个一维数组
				
			每个一维数组中有几个元素呢？
				不确定
	
	格式三：
		数据类型[][] 数组的名字 = {{元素1,元素2,......},{元素1,元素2,......},... ...};
			
			int[][]     arr     = {{1,2}, {3,4,5}, {6}};
			
			二维数组中有几个一维数组？
				3个
	
			每个一维数组中有几个元素？
				2
				3
				1

二维数组的使用？
	1.创建容器
		int[][] arr = new int[3] [2];
	
	2.存数据
		arr[0] [0] = 1;
		arr[0] [1] = 2;
		arr[1] [0] = 3;
		arr[1] [1] = 4;
		arr[2] [0] = 5;
		arr[2] [1] = 6;
	
	3.取数据
		System.out.println(arr[0] [0]);
		System.out.println(arr[0] [1]);
		System.out.println(arr[1] [0]);
		System.out.println(arr[1] [1]);
		System.out.println(arr[2] [0]);
		System.out.println(arr[2] [1]);

二维数组的遍历？
	int[][] arr = {{1,2},{3,4,5},{6,7,8,9}};

​	for(int i = 0; i < arr.length; i++) {
​		for(int j = 0; j < arr[i].length; j++) {
​			System.out.print(arr[i] [j] + " ");
​		}
​		System.out.println();
​	}

## 方法（函数）

#### 1.方法（day6）

什么是方法？
		具有(特定功能)一段独立的小程序(代码块)
		

方法的作用？
	1.提高了代码的复用性
	2.提高了代码的维护性

方法的定义格式？
	修饰符 返回值类型 方法名字(数据类型 变量名, 数据类型 变量名, ... ...) {
		语句体内容;
		return 返回值;
	}
	
怎么写一个方法？
	修饰符：目前为止，固定格式：public static
	
	返回值类型：???
	
	方法名字：标识符，我们自己起的
	
	参数列表：???
	
	语句体内容：实现功能的代码
	
	return 返回值：???
	
	两个明确：
		1.明确参数列表
		2.明确返回值类型
		
	例子：
		需求：定义一个方法，该方法的功能是获取两个整数和？
			public static int getSum(int i, int j) {
				int sum = i + j;
				return sum;
			}

方法的使用？
	方法只有被调用才会执行，不调用是不会执行的
	
	怎么调用？
		1.单独调用
			方法名(参数);
			
			注意：如果方法有返回值，使用单独调用是没有意义的
				  如果方法没有返回值，使用单独调用就有意义了
		
		2.输出调用
			System.out.println(方法名(参数));
			
			注意：如果方法没有返回值，就不能使用输出调用
		
		3.赋值调用
			数据类型 变量名 = 方法名(参数);
			
			注意：如果方法没有返回值，就不能使用赋值调用


​	

我们能遇到哪些返回值类型的方法？
	基本数据类型：4类8种
		public static byte aaa() {
			return 1;
		}
		
		public static short bbb() {
			return 1;
		}
		
		public static int ccc() {
			return 1;
		}
		
		public static long ddd() {
			return 1;
		}
		
		public static float eee() {
			return 1.2;
		}
		
		public static double fff() {
			return 1.2;
		}
		
		public static char ggg() {
			return 'a';
		}
		
		public static boolean hhh() {
			return true;
		}

​	引用数据类型：String、、数组、、类类型(返回值为对象)
​		public static String iii() {
​			return "约吗";
​		}
​		
​		public static int[] jjj() {
​			int[] arr = {1,2,3};
​			return arr;
​		}
​		public static 类名 kkk() {
​			int[] arr = {1,2,3};
​			return arr;
​		}
​		
​	特别的返回值类型：void
​		public static void kkk() {
​			return;
​		}

方法的注意事项？
	1.方法与方法之间是平级关系，不能嵌套定义
		public static void aaa() {
			public static void bbb() {
			
			}
		}
		
	2.方法的返回值类型和返回值匹配
		public static int aaa() {
			return true;
		}
		
		public static int aaa() {
			return 1.2;
		}
		
		public static String aaa() {
			return 1;
		}
		
		以上三种写法是错误的
	
		public static double aaa() {
			return 1;
		}
		
		public static int aaa() {
			return 'a';
		}

​		public static char aaa() {
​			return 1;
​		}
​		
​		以上三种写法是正确的

​	3.如果方法没有返回值的时候，返回值类型要写void
​		void：是一个关键字，不是一个数据类型，它只能写在返回值类型的位置，代表没有返回值的意思

​		注意：
​			1.当方法的返回值类型为void的时候，只能使用单独调用
​			2.当方法的返回值类型为void的时候，return;可以省略不写
​				return关键字有什么用？
​					1.可以返回一个数据，哪里调用返回到哪里
​					2.作为方法的结束标记
​						public static int getSum() {
​							return 1;
​							System.out.println("约吗");
​						}
​						
​						在同一对花括号内，return下面不能有任何语句，因为永远都执行不到
​		

-----------------------------------------

​						public static int getSum() {
​							if(3 > 2) {
​								return 1;
​							}
​							
​							System.out.println("约吗");
​						}
​						
​						如果不进入到if，就没有return了
