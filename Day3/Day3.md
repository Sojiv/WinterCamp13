﻿几何和暴力法专题
--------
几何side
========
直线的参数方程：已知直线上两点P1,P2
直线上点P=P1+t*(P2-P1)
t<0在P2 P1射线上，
0<t<1在P1 P2线段上，
t>1在P1 P2射线上（不包含P1P2线段）


CERC2012 LA 6263
n条直线分割若干区域，求未撒点区域数

IPSC部分题解
--------
##IPSC2012 Fair coin toss##
对于一个集合，使它公平的充分必要条件就是含有概率为0.5的硬币。

显然，这个对于充分条件是显然易证的。
对于必要条件，若两个概率反面向上分别为(0.5+a)和(0.5+b)

那么总共反面向上就(0.5+a)(0.5+b)+(0.5-a)(0.5-b)

=0.25+0.5a+0.5b+ab+0.25-0.5b+ab=0.5+2ab a,b≠0
##IPSC2012 Evil matching##
首先我们因为发现所有的数字的总和很小，所以可以考虑这样的存储。
对于整数x，我们使用str(1<<(x-1))表示，例如1→1，2→10，3→100

这样的话就是一个很简单的匹配问题喵~

后两问嘛……多项式乘法貌似（这不是坑爹吗？）

##IPSC2011 BFS killer##
显然是尽量制造大的分形来卡别人。

四叉分形可以过Easy。如果使用一个高效利用空间的二叉分形应该可以过Hard

（建议保留这个用于Codeforces，深藏功与名）
##IPSC2011 Inverting bits##
压位的技巧就不用说了吧……
```
000→111 
001→110 
010→101 
011→100 
100→011 
101→010 
110→001 
111→000 
ex3=A & B & C //3个全是1
mo1=A | B | C //至少一个是1
mo2=(A & B)|(B & C)|(A & C) //至少两个是1
l1=! mo2 //不多于一个1
ex1=le1 & mo1 //正好一个为1
ex13=ex1 | ex3 //正好1或3个
ex02=! ex13 //正好0或2个
ex0=ex02 & l1 //正好0个
ex2=ex02 & mo2 //正好2个
!A = ex0 | (ex1 & (B | C)) | (ex2 & (B & C))
!B = ex0 | (ex1 & (A | C)) | (ex2 & (A & C))
!C = ex0 | (ex1 & (A | B)) | (ex2 & (A & B))
```
##IPSC2011 Keep clicking,keep flipping##
（坑）
##IPSC2010 Flawed Code##
勇敢的少年啊快去CF hack啊~（没啥好讲的，不过好喜欢的题型）
##IPSC2007 Guess the Numbers##
很显然，使用7次可以猜出所有奇数位的全部和偶数位的部分

之后，使用两次可以通过这样的堆叠来求出那些被遮挡住的偶数位
##IPSC2002 Space Suckers##
显然可以发现，因为可以任意交换列的顺序，所以说我们可以很显然地去考虑这样的想法：

对于这样的问题，凡是可以参加任意交换的都要将其放入同一个集合之中。

最后每一次要让那些1汇合在一起（既要让他们的集合互相之间组成一个连续的段）

##IPSC2006 Gotta Pick'em All##
在经过一段爆搜之后大概可以发现，对于较大的n的话，偶数（N=2K）都等于1（ K..2K）
奇数（N=2K+1）都等于4（
1,3,...,2K=1;
K,K_1,k+2,...,2K;
K,K+2,K+3,...,2K+1;
K+1,k+2,...,2K+1;
）

##IPSC2012 Card Game##
记忆化搜索的话，内存占用将会是9G

然而考虑到根本不需要考虑13（看到了直接拿走），实际只会有2G

（不过这的确是一个更新电脑的理由啊路~）
