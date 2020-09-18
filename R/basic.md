# R初学习

R 语言是为数学研究工作者设计的一种数学编程语言，主要用于统计分析、绘图、数据挖掘。  
R 语言与 C 语言都是贝尔实验室的研究成果，但两者有不同的侧重领域，R 语言是一种解释型的面向数学理论研究工作者的语言，而 C 语言是为计算机软件工程师设计的。  
R 语言是解释运行的语言（与 C 语言的编译运行不同），它的执行速度比 C 语言慢得多，不利于优化。但它在语法层面提供了更加丰富的数据结构操作并且能够十分方便地输出文字和图形信息，所以它广泛应用于数学尤其是统计学领域。

+ R 语言特点
	+ R 语言环境软件属于 GNU 开源软件，兼容性好、使用免费
	+ 语法十分有利于复杂的数学运算
	+ 数据类型丰富，包括向量、矩阵、因子、数据集等常用数据结构
	+ 代码风格好，可读性强

+ 变量
R 语言的有效的变量名称由字母，数字以及点号 . 或下划线 _ 组成，变量名称不得以数字开头。

## 基本操作
1.变量赋值
```R
# 注意：R 语言赋值使用的是左箭头 <- 符号，不过一些新版本也支持等号 =。
myString <- "Hello, World!"

# 查看已定义的变量使用 ls() 函数：
print(ls())

# 删除变量使用 rm() 函数：
rm(var.3)
```

2.输入输出
+ print() 输出
```R
# print() 是 R 语言的输出函数。
print("RUNOOB")
print(123)
```

+ cat() 函数
```R
# 输出结果的拼接使用 cat() 函数
print("RUNOOB")
cat(1, "加", 1, "等于", 2, '\n') 	# 1 加 1 等于 2
```

+ 输出内容到文件
```R
# cat() 函数支持直接输出结果到文件
# 这个语句不会在控制台产生结果，而是把 "RUNOOB" 输出到 "/Users/runoob/runoob-test/r_test.txt" 文件中去。file 参数可以是绝对路径或相对路径，建议使用绝对路径，
cat("RUNOOB", file="/Users/runoob/runoob-test/r_test.txt")
cat("RUNOOB", file="D:\\r_test.txt")
# 注意：这个操作是"覆盖写入"操作，请谨慎使用，因为它会将输出文件的原有数据清除。如果想"追加写入"，请不要忘记设置 append 参数：
cat("GOOGLE", file="/Users/runoob/runoob-test/r_test.txt", append=TRUE)

# sink() 函数可以把控制台输出的文字直接输出到文件中去：
# 注意：这个操作也是"覆盖写入"操作，会直接清除原有的文件内容。如果我们依然像保留控制台的输出，可以设置 split 属性：
sink("/Users/runoob/runoob-test/r_test.txt", split=TRUE)

# 如果想取消输出到文件，可以调用无参数的 sink ：
sink()
```

+ 从文件读入文字
```R
# 如果纯粹的想将某个文件中的内容读取为字符串，可以使用 readLines 函数：
readLines("/Users/runoob/runoob-test/r_test.txt")
# 注意：所读取的文本文件每一行 (包括最后一行) 的结束必须有换行符，否则会报错。
```

3.工作目录
```R
# 当前工作目录
print(getwd())

# 设置当前工作目录
setwd("/Users/runoob/runoob-test2")
```

## 数学函数
数学函数 |	说明
-- |--
sqrt(n)	 |	n的平方根
exp(n)	 |	自然常数e的n次方，
log(m,n) |	n的对数函数，返回n的几次方等于m
log10(m) |	相当于log(m,10)
round(n, m) |	对 n 保留 m 位小数四舍五入
ceiling	(n) |	对 n 向上取整
floor(n) |	对 n 向下取整








