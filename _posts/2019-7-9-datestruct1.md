---
layout:     post
title:      "数据结构题目"
subtitle:   "数据结构"
date:       2019-07-8 10:00:00
author:     "zl"
header-img: "img/post-bgos-2019.jpg"
tags:
    - 期末复习总结系列
---

## 第一章：

### 判断：
1.	数据元素是数据的基本单位。
2. 	数据项是数据的最小单位。
3. 数据的逻辑结构独立于计算机，物理结构依赖于计算机。
4. (×)每种数据结构都应该具备三种基本运算：插入、删除和查找。
5. 数据元素可以由类型互不相同的数据项构成。
6. (×)数据结构的抽象操作的定义与具体实现有关。

 选择：   
1. 	被计算机加工的数据元素不是孤立无关的，它们彼此之间一般存在着某种联系。通常将数据元素之间的这种联系称为______。
A. 规则 
2.	设n是描述问题规模的非负整数，下面程序段的时间复杂度是______。

    ```x=2;
    while(x<n/2)  x=2*x;
    ```
    A. O(log2n)

3. 	求整数n（n>=0）阶乘的算法如下，其间复杂度是______。
   
     ```
    int fact(int n) {
      if(n<=1)  return 1;
      return  n*fact(n-1);
    }

    ```
     B. O(n)     

4. 可以用**抽象数据类型**定义一个完整的数据结构。
5. 15．	计算算法的时间复杂度是属于一种______。  
     B. 事前分析估算的方法  

6. 21．	数据元素之间的关系在计算机中有两种不同的表示方法______。
   D.  顺序存储和非顺序存储

7. 23．	以下属于逻辑结构的是____C__。
A.  顺序表     B. 哈希表      C.  有序表      D.  单链表


### 填空：  

1. 算法的主要特点：确定性，有限性，可行性，零个或零个以上输入，一个或一个以上输入。

2. 2．	计算机执行下面语句时，语句S的频度（执行次数）为________。
3. for(i=1;i<n-1;i++)  for(j=n;j>=i;j--)  S;
   S执行次数：(n+3)(n-2)/2
   
### 应用题：

1. 有如下递归函数，请分析其时间复杂度。
```
fact(int n)
{
  if（n<=1）  return 1;  (1)
  else  return (n*fact(n-1));  (2)
}
```
设fact(n)的运行时间函数是T(n),语句(1)的运行时间为O(1),语句(2)的运行时间为T(n-1)+O(1),所以

```
T(n)=   O(1)  n<=1
T(n-1)+O(1)  n>1

所以,T(n)= O(1)+T(n-1)  =2*O(1)+T(n-2)  =…
     =(n-1)*O(1)+T(1)  =n*O(1)  =O(n)
     
```


## 第二章 

### 判断：
1. 线性表的链式存储结构的特点是用一组任意的存储单元存储线性表的数据元素。
2. 线性表中的元素可以是各种各样的，但同一线性表中的数据元素具有相同的特性，因此是属于同一数据对象。
3. 在线性表的顺序存储结构中，逻辑上相邻的两个元素但在物理位置上并不一定相邻。（× ）
4. 单链表是随机存取的存储结构。（× ）
5. 静态链表既有顺序存储的优点，又有链式存储的优点。所以，它存取表中第i个元素的时间与i无关。（ 错）（静态链表没有用到指针。需要遍历）

### 选择：
1. 线性表是________。   
A. 一个有限序列，可以为空       
2. 向一个有127个元素的顺序表中插入一个新元素并保持原来顺序不变，平均要移动的元素个数为________。        
     B．63.5  
3. 对于顺序存储的线性表，设其长度为n，在任何位置上插入或删除操作都是等概率的。删除一个元素时所需移动元素次数的期望值为   
     C. (n-1)/2   
4. 单链表的存储密度________。   
     C．小于1 
5. 设单链表中指针p指向结点A，若要删除A之后的结点（若存在），则需修改指针的操作为________。  
A．p->next=p->next->next 
6. 将两个各有n1和n2个元素的有序表(递增)归并成一个有序表，仍保持其递增顺序，则最少的比较次数是________。         
  D．min(n1,n2)
7. 18．	能在O（1）时间内访问线性表的第i个元素的结构是________。     
A. 顺序表

8. 19．	单链表中，增加一个头结点的目的是________。  
    C. 方便运算的实现  
9. 20．	若有指定的n个元素，则由这n个元素建立一个有序单链表的时间复杂度的量级是________。    
       C．O(n2)    
10. 链表不具有的特点是________。    
      B．可随机访问任一元素
11. 24．	某线性表中最常用的操作是在最后一个元素之后插入一个元素和删除第一个元素，则采用________存储方式最节省运算时间。  
      D．仅有尾指针的单循环链表

### 填空：
1. 有一个含头结点的单循环链表，头指针为head，则判断其是否为空的条件为： head->next=head


## 第三章

### 判断：
1. 栈和队列都是限制存取点的线性结构。
2. 设栈采用顺序存储结构。若已有i-1个元素入栈，则将第i个元素入栈时，入栈算法的时间复杂性为O（i）。  （ ×）
3. 中缀表达式：（a+b）*d+e/(f+a*d)+c的后缀表达式为：ab+d*efad+/*+c+。（ ×）

### 选择：
1. 若已知一个栈的入栈序列是1,2,3,…,n,其输出序列为s1,s2,s3,…sn,若s1=n, 则si为________。  
    C．n-i+1 
2. 一个递归算法必须包括________。  
      B. 终止条件和递归部分
3. 设有一个递归算法如下
```
int fact(int n) {  //n大于等于0
 if(n<=0) return 1;
 else return n*fact(n-1);
}
```
则计算fact(n)需要调用该函数的次数为________。 
A． n+1 

4. 在一个具有n个单元的顺序栈中，假设以地址高端作为栈底，以top作为栈顶指针，则当作进栈处理时，top的变化为________。  
     C．top--  

5. 循环队列用A[0..m-1]存放其元素值，用front和rear分别表示队头和队尾，那么当前队列中的元素个数是________。
A．(rear-front+m)%m   
6. 循环队列存储在数组A[0..m-1]中，则出队时的操作为________。
  D. front=(front+1)%(m+1)
7. 循环队列存储在数组A[0..m]中，则入队时的操作为________          D. rear=(rear+1)%(m+1) 
8. 18．	与中缀表达式a*b+c/d-e等价的前缀表达式是________。   
A．-+*ab/cde  
9. 	为解决计算机主机与打印机间速度不匹配问题，通常设一个打印数据缓冲区。主机将要输出的数据依次写入该缓冲区，而打印机则依次从该缓冲区中取出数据。该缓冲区的逻辑结构应该是________。  
A．队列   

10. 已知循环队列存储在一维数组A[0..n-1]中，且队列非空front和rear分别指向队头元素和队尾元素。若初始时队列为空，且要求第1个进入队列的元素存储在A[0]处，则初始时front和rear的值分别是________。B  
A．0,0           B．0，n-1          C．n-1,0         D．n-1,n-1  

### 填空题

1. 设SS\[1..maxsize]为一个顺序存储的栈，变量top指示栈顶元素的位置，当栈未满时，将元素e压入栈需执行下列语句：top++ 和 SS\[top]=e

2. 设顺序栈存放在s.elem\[0…m-1]中，栈顶指针为 s.top，栈底位置是m-1,则栈空条件是__( s.top==m),栈满条件是 s.top==0。
3. 为了增加内存空间的利用率和减少发生上溢的可能性，由两个栈共享一片连续的内存空间时，应将两栈的 **栈底**分别设在这片内存空间的两端，这样，只有当**两栈栈顶相遇**时，才产生上溢。
4. 设循环向量有m个元素，循环向量中有一个循环队列。在循环队列中，设队头指针front指向队头元素，队尾指针rear指向队尾元素后的一个空闲单元。则在循环队列中，队满标志为 **(rear+1)%m==front**，队空标志为**front==rear**
5. 数组Q[n]用来表示一个循环队列，f为当前队列头元素的前一位置，r为队尾元素的位置，假定队列中元素的个数小于n，计算队列中元素个数的公式为 **(n+r-f)%n**

6. 多个栈共存时，最好用(**链式存储结构** )作为存储结构。
7. 9．	若已知一个栈的入栈序列是1,2,3,...,n，其输出序列为p1,p2,p3,...,pn，若p1=n，则pi为(**n-i+1** )



## 第四章
### 判断题
1. KMP算法的特点是在模式匹配时指示主串的指针不会变小。
2. 串是一种数据对象和操作都特殊的线性表。
3. 字符串“aababaaaba”的next数组的值是-1 0 1 0 1 0 1 2 2 3。

### 选择题
1. 串是一种特殊的线性表，其特殊性体现在________。   
     B．数据元素是一个字符 
2. 已知字符串s为”abaabaabacacaabaabcc”，模式串t为”abaabc”，采用KMP算法进行匹配，第一次出现“失配”（s[i]!=t[i]）时,i=j=5，则下次开始匹配时，i和j的值分别是________。   
    C. i=5,j=2    
3. 若串S=”myself”，其子串的数目是________。
     C. 22  

### 填空题

1. 串的机内常用存储方式有三种：定长顺序串、 __(**堆串** )_ 和块链串。
2. 2．	子串的定位又称为串的（**模式匹配**）_。 
3. 3．	下列是简单的模式匹配算法程序，请补充完整（注：该函数要求返回子串T在主串S中第pos个字符之后的位置，若不存在，则函数的值为0）。
```
int Index(Sstring *S, Sstring *T,int pos) {
  i=pos-1;  j=0;
  while(i<S->len&&j<T->len) {
    if( T->ch[i]==S->ch[j] ) { __( )__ ; j++; }  
    else  { i= __( )__ ; j=0; }   
  }
  if(j==T->len)  return i-T->len+1;
  else  return 0;
}
```
i++; i-j+1;

4. 两个字符串相等的充分必要条件是__(**串的长度相等并且两串对应字符相等** )__。
   
### 算法应用题
1. 给出以S=’aabcbabcaabcaaba’为目标串，T=’abcaaba’为模式串的KMP快速匹配过程。
   
   KMP匹配算法的基本思想是：当模式串字符和主串字符失配时，指向珠串的指针不懂，而是改变模式串指针的指向，使指向模式串的指针尽可能指向模式串靠右的字符。

## 第五章 数组与广义表
### 判断题：
1. 从逻辑结构上看，n维数组的每个元素均属于n个向量。
2. 稀疏矩阵压缩存储后，必会失去随机存取功能。
3. 一个广义表可以为其他广义表所共享。

4. 数组A\[0..5,0..6]的每个元素占5个字节，将其按列优先次序存储在起始地址为1000的内存单元中，则元素A\[5,5]的地址是______。A   
A．1175    B．1180     C．1205     D．1210 
> LOC\[5,5]=\[(5-0)*6+(5-0)]*5+1000=1175
5. 假设以行序为主序存储二维数组A=array\[1..100,1..100]，设每个数据元素占2个存储单元，基地址为10，则LOC\[5,5]=（  ）。B  
A．808            B．818             C．1010             D．1020
> LOC\[5,5]=\[(5-1)*100+(5-1)]*2+10=818

6. 9．	设二维数组A[1.. m，1.. n]（即m行n列）按行存储在数组B[1.. m*n]中，则二维数组元素A[i,j]在一维数组B中的下标为（  ）。  
    A．(i-1)*n+j

7. 10．	数组A[0..4,-1..-3,5..7]中含有元素的个数（  ）。     
   B．45  

8. 12．	广义表((a,b,c,d))的表头和表尾分别是（  ）。     
    B．(a,b,c,d)和( ) 
    
9. 14．	用数组r存储静态链表，结点的next域指向后继，工作指针j指向链中结点，使j沿链移动的操作为（ ）。    
A. j=r[j].next 

### 填空题
1. 一个n*n的对称矩阵，如果以相同的元只存储一次的原则进行压缩存储，则其压缩后的存储容量为(**n(n+1)/2** )。
2. 设n行n列的下三角矩阵A已压缩存储到一维数组B[0..n(n+1)/2-1]中，且按行为主序存储，则aij（i,j=0,1,2,…,n-1，且i≥j）对应的B中的存储位置为__( )__。 
> 1+2+...+i+j=**i(i+1)/2+j**
3. 设n行n列的下三角矩阵A已压缩存储到一维数组B[1..n*(n+1)/2]中，且按行为主序存储，则aij（i,j=1,2,…,n-1，且i≥j）对应的B中的存储位置为__( )__。
> 1+2+...+(i-1)+j=**i(i-1)/2+j**
4. 设n行n列的上三角矩阵A已压缩存储到一维数组B[0..n(n+1)/2-1]中，且按行为主序存储，则aij（i,j=0,1,2,…,n-1，且i≤j）对应的B中的存储位置为__( )__。
> n+(n-1)+...+\[n-(i+1)]+j-i=**(2n-i+1)i/2+(j-i)**
5. 设n行n列的上三角矩阵A已压缩存储到一维数组B[1..n*(n+1)/2]中，且按行为主序存储，则aij（i,j=1,2,…,n-1，且i≥j）对应的B中的存储位置为__( )__。
> (2n-i+2)(i-1)/2+(j-i+1)

6. 三元组表是__(**稀疏矩阵** )__的一种压缩顺序存储结构。

































