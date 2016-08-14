---
layout: post
title: python 统计文件个数脚本
category: note
tags: python 
---
## 场景

想知道放在某个server 上面所有测试用例的个数（测试用例都是创建为sample.xml的格式文件）

## 脚本目的

统计某目录下所有子文件夹中xxx.xml 的个数


## python 脚本实现

```python
import os,shutil

#print os.getcwd()


sourceRootFolder="D:\Automation\TestSuites\polaris"

count=0
filecount=0

for f in os.listdir(sourceRootFolder):
  tmpdir=os.path.join(sourceRootFolder, f)
  if f.startswith("T"):
    count=count+1
    newpath=os.path.join(tmpdir,"Scenarios")
    print (newpath)
    for sf in os.listdir(newpath):
      if os.path.isfile(os.path.join(newpath,sf))  and sf.endswith(".xml") :
        filecount=filecount+1


print (count," test suites in total")
print (filecount,"test Scenarios in total")
```
