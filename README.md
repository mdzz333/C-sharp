# C sharp

#### 项目介绍
传智播客：C#教程

#### 参与贡献

1. Fork 本项目
2. 新建 Feat_xxx 分支
3. 提交代码
4. 新建 Pull Request

1. 使用 Readme\_XXX.md 来支持不同的语言，例如 Readme\_en.md, Readme\_zh.md


记得将git的邮箱改成和码云或者github的账户邮箱一致的时候，push代码才算在贡献中！

2018.12.8
	开始新建分支，以后每一章节新建一个分支
2018.12.14	
	创建本地分支并切换	git checkout -b 07_FlightChess
	推送到远程分支		git push origin 07_FlightChess
2019.1.13
1、值传递和引用类型传递
	string s1 = "张三";
	string s2 = s1;
	s2 = "李四";
	Console.WriteLine(s1);//张三
	Console.WriteLine(s2);//李四
	//string比较特殊，具有不可变性，每次重新赋值都会开辟新的空间
	//具体分析(自己分析，加深理解)
	&s1
	0x00efeea8//栈地址
	*&s1: 0x030023c4//堆地址
	&s2
	0x00efeea4//栈地址
	*&s2: 0x030023c4//堆地址
	string s2=s1的时候，他们指向同一个堆空间。
	但是s2="李四"的时候,
	&s2
	0x00efeea4//栈地址
	*&s2: 0x030023d8//堆地址
	它新开辟了一个堆空间写入"李四"，并且让s2指向新的对空间
	所以s1的值没变还是张三
	s2的值变了，变成一个新的李四
	
	
2、'protected'和'protected internal'有什么区别？ ❓  #问题
	protected表示“仅此类和派生类”。
	internal意味着“只有这个程序集中的类”。
	protected internal表示“ protected OR internal ”（同一程序集中的任何类，或任何派生类 - 即使它位于不同的程序集中）。
	即它并不意味着“保护和内部”（同一个组件内只有派生类）。
	
	
	
	
	
	