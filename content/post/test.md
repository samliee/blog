+++
title = 'Test'
date = 2024-09-27T13:43:05+08:00
draft = false
+++
## 习题2.1 简单计算器 (20分)

模拟简单运算器的工作。假设计算器只能进行加减乘除运算，运算数和结果都是整数，四种运算符的优先级相同，按从左到右的顺序计算。

**输入格式:**
输入在一行中给出一个四则运算算式，没有空格，且至少有一个操作数。遇等号”=”说明输入结束。

**输出格式:**
在一行中输出算式的运算结果，或者如果除法分母为0或有非法运算符，则输出错误信息“ERROR”。

**输入样例:**

```c
1+2*10-10/2=
```

输出样例:

```c
10
```

这道题不要求判断运算符的优先级，不用栈就可以完成任务。将第一个数字和第一个操作符特殊化，这样后面的运算就可以用循环实现。

```c
#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>

int
main( int argc , char **argv )
{
    int a;
	int i, j;
	int result;
    
	char op;
	char exp[100];
	char n[10];		//用于单独提取操作数
    
	scanf("%[^=]", exp);	//从流中读入文本, 当读入=时结束并吐出=
	/*
	** 求result的初始值
	*/
	for( i = 0; exp[i] != '\0'; i++ ){
		if( isdigit( exp[i] ) ){
			n[i] = exp[i];
		}else{
			break;
		}
	}
	n[i] = '\0';
	sscanf( n, "%d", &result );	//将字符串n转换为整型数据存储到result中
	op = exp[i];				//取第一个操作符
	/*
	** 求result和操作符的初始值
	*/
	for( i++, j = 0; exp[i] != '\0'; i++ ){
		if( isdigit( exp[i] ) ){
			n[ j++ ] = exp[i];
			if( exp[ i+1 ] != '\0' ){	//当读到最后一个操作数不continue, 进入计算
				continue;
			}
		}
		n[j] = '\0'; 
		sscanf( n, "%d", &a );
		j = 0;
		switch( op ){		//操作符op是当前操作符的前一个
			case '+':
				result += a;
				break;
			case '-':
				result -= a;
				break;
			case '*':
				result *= a;
				break;
			case '/':
				if( 0 == a ){
					printf("ERROR");
					exit(0);
				}else{
					result /= a;
				}
				break;
			default:
				printf("ERROR");
				exit(0);
		}
		op = exp[i];
	}
	printf("%d", result);

    return 0;
}
```


