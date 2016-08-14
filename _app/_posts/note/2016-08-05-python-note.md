---
layout: post
title: python note
category: note
tags: python
---

 

1. install

* website: https://www.python.org/
* version: 2.7.1
* install: run the msi install package and do not forget to check the options of "pip" and "add python.exe to Path"
* path: C:\Python27
* exit() 
* excute python file  in Mac/Linux start with

```sh
#!/usr/bin/env python　
```

2. cons

解释性语言，运行慢
无法加密

3. basic

  a. input/output

```python
name=raw_input("enter your name:")
print "hi",name
```

  b. 缩进的语句视为代码块
  
  c. 大小写敏感

  d. 转义字符\ 标识字符串内部特殊字符

```python
print "I\'m learning \nPython"
print r"I\'m learning \nPython"
print """line1
line2
line3
"""
```
  e. 全部大写的变量名表示常量

  f. 编码 

  源码中包含中文的时候，保存用UTF-8 编码（可变长编码），文件头添加以下两行， 用于读取源码时使用UTF-8编码读取文本


```python
#! /usr/bin/env python
# -*- coding: utf-8 -*-

print u"这".encode("utf-8")
```

  g. 格式化

  %用来格式化字符串

```python
print "hi, %s aged %d" %("day", 25)
```
  h. list

  一个有序可变的列表

```python

line1=["lily", 23, True]
team=["a","bcd",line1]
print len(team)

#access the element
print team[2][2]
print "the first element %s" %(team[0])
print  "last element %s and the second last element %s" %(team[-1],team[-2])

#add/insert element
team.append("ij")
team.insert(1,"someone")
print team

#delete element 
team.pop()
print team
team.pop(0)
print team

#replace element
team[2]="newone"

print team

#empty list
emptyteam=[]
print len(emptyteam)
```
  不可变的列表tuple，初始化后不改变，无append/insert 等方法，代码更加安全

```python
#tuple
row=("to","two",2)

#tuple with one element
row2=(1,)

print row[2]
```
  i. 条件判断

```python
birth=int(raw_input("birth:"))
if birth>2000:
  print "child of", birth
elif birth>1990:
  print "young of", birth
else:
  print "old", birth
```
  j. 循环

```python
#for 
sum=0
for x in range(101):
  sum=sum+x
print sum

#while 
sum=0
n=99
while n>0:
  n=n-2
  sum=sum+n
print sum
```
k. dictionary
key-value 存储方式

```python
#dictionary
roster={'angel':10,'simon':20,'tony':30}
print roster['simon']

#delete key
roster.pop('tony')
print roster

#set which store key only
s=set([1,2,3])
s.add(4)
print s

s.remove(4)
print s
```
　