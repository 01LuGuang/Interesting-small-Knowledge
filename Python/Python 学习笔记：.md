# Python 学习笔记：



## 一 基础语法

 1.help()查看对象帮助信息

2.dir()查看对象的属性和具有的方法

3.id()查看变量地址

4.type()查看对象数据类型

5.print(), input(),  del()删除内存中的对象，len()长度



## 二 数据类型

Number（数值）String（字符串） List（列表），Tuple（元组）Dictionary（字典） Set（集合）

##### 1.Number：

int，float，bool，complex（x + yj复数）

*数值计算：*

+，-，*，/，%，//（取整）**（乘方）注：不同类型的数字计算时，结果类型为精度较高的类型

*计算函数：*

abs(), round()四舍五入, divmod(y,x)返回两个数值的商和余数， sum,max,min

##### 2.数据常用操作：

***数据引用**产生的问题：*

![9ca642a522c565fec26e016ed44f0b7](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/9ca642a522c565fec26e016ed44f0b7-1714060167032-2.jpg)

![e60d495212f4280f7380f344906b990](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/e60d495212f4280f7380f344906b990-1714060233784-5.jpg)



解决方案：浅拷贝copy()和深拷贝deepcopy()

![9cbe8d7ee43f702f1c46243fb079269](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/9cbe8d7ee43f702f1c46243fb079269-1714060242519-8.jpg)

![e27d634a248ce0b2e0d820d021cbc08](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/e27d634a248ce0b2e0d820d021cbc08-1714060284448-11.jpg)



## 三 数据结构

略



### 1 print函数

输出内容在文件中

```
fp = open('mpf.txt','w')
print('hello mpf!',file=fp)
fp.close()
```

![屏幕截图 2024-04-26 003446](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-26%20003446-1714062969438-17.png)

print函数自带换行，加一个end可以同一行输出

```
print('mpf能不能', end='')
print('一周学会python')
```

连接符：相同类型连接

`print('mpf'+' 2024 4 26')`



### 2 input函数

`x=input('提示文字')`

无论输入的是什么，x变量均为字符串类型

```
num=input('请输入一个数字：')
print('输入的数字是：'+num)  # num为字符串
num=int(num)
print('输入的数字是：',num) # num为int
```



### 3  字符串

![31da0e8d38d33511597ad4a1ea2e397](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/31da0e8d38d33511597ad4a1ea2e397-1714064683649-20.png)

**\t：**一个制表位8位，前面字符不足八位补足8位。

##### 1.字符串的索引和切片[]:

```
s='HELLOWORLD'
print(s[0],s[-10])  #s[0]和s[-10]指的是同一个字符
print('北京欢迎您'[4])
print(s[2:7])   #正向截取字符串[2,7)
print(s[-8:-3]) #反向
print(s[:5])    #默认字符串开始0
print(s[3:])    #默认字符串结尾\0
```

##### 2.字符串常用操作：

![屏幕截图 2024-04-29 191804](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20191804-1714389666099-2-1714389667435-4.png)

### 4 布尔类型

```
x=True
print(x)
print(x+1)  # 1+1
print(type(x))
print(False + 10)  # 0+10
print(bool(18))  # 非零的整数的bool值为True
```

![屏幕截图 2024-04-29 192441](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20192441-1714389930529-7.png)



### eval函数



![屏幕截图 2024-04-29 194212](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20194212-1714391171693-10.png)

```
height=input('请输入身高')
print(height,type(height))
age=eval(input('请输入您的年龄'))
print(age,type(age))
```

![屏幕截图 2024-04-29 194542](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20194542-1714391177955-13.png)





### 5 运算符

![屏幕截图 2024-04-29 194650](D:/Code/NoteDocument/Typora/Python%E5%AD%A6%E4%B9%A0/Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20194650.png)

<img src="D:/Code/NoteDocument/Typora/Python%E5%AD%A6%E4%B9%A0/Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20194748.png" alt="屏幕截图 2024-04-29 194748" style="zoom:75%;" />

![屏幕截图 2024-04-29 194805](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20194805-1714393926455-2.png)![屏幕截图 2024-04-29 194757](D:/Code/NoteDocument/Typora/Python%E5%AD%A6%E4%B9%A0/Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20194757.png)

![屏幕截图 2024-04-29 195048](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20195048-1714393940222-5.png)

![屏幕截图 2024-04-29 195119](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20195119-1714393944118-8.png)

![屏幕截图 2024-04-29 195140](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20195140-1714393948473-11.png)

![屏幕截图 2024-04-29 195159](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20195159-1714393954147-14.png)

![屏幕截图 2024-04-29 195307](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20195307-1714393961068-17.png)





## 三 程序



#### 程序语句

##### 1.选择结构

if 表达式：

​	语句

**（1）多分支结构：**

<img src="./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20205828-1714395566890-20.png" alt="屏幕截图 2024-04-29 205828" style="zoom:75%;" />





**（2）嵌套if**

![屏幕截图 2024-04-29 210048](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20210048-1714395682366-23.png)

**（3）模式匹配（相当于switch）**

```
score=input('请输入成绩等级：')
match score:
        case 'A':
            print('优秀')
        case 'B':
            print('良好')
        case 'C':
            print('及格')
        case 'D':
            print('不及格')
```



##### 2.循环结构

***for循环***

![屏幕截图 2024-04-29 211610](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20211610-1714397394931-26.png)

```
# 遍历字符串
for i in 'hello':
    print(i)
# range()函数，Python中的内置函数，产生一个[n,m)的整数序列
for i in range(1,11):
    print(i)
    if i%2==0:
        print(i,'是偶数')
```



***while循环***

![屏幕截图 2024-04-29 212911](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-04-29%20212911-1714397423514-29.png)

```
s=0
i=1
while i<=100:
    s+=i
    i+=1
print('1-100的和为： ',s)
```



#### 代码实战1：打印菱形

```
# 打印菱形
row = eval(input('请输入菱形的行数：'))
while row % 2 == 0:
    print('重新输入：')
    row = eval(input('请输入菱形的行数：'))
top_row = (row+1)//2
for i in range(1, top_row+1):
    for j in range(1, top_row+2-i):
        print(' ', end="")
    for k in range(1, i*2):
        print('*', end="")
#打印空心菱形：打印*时首尾打印就行，否则打印' '
   # for k in range(1, i*2):
    #     if k == 1 or k == i*2-1:
    #         print('*', end="")
    #     else:
    #         print(' ', end="")
    print('')
bottom_row = row//2
for i in range(1, bottom_row+1):
    for j in range(1, i+2):
        print(' ', end="")
    for k in range(1, (bottom_row+1-i)*2):
        print('*', end="")
    print('')
```



#### 空语句pass

![屏幕截图 2024-05-01 132528](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20132528-1714541519988-2.png)

```
if True:
    pass
# while True:
#     pass
for i in range(10):
    pass
```



#### 代码实战2：9*9乘法表

```
# 9*9乘法表
for i in range(1,10):
    for j in range(1,i+1):
# 注意连接符"+"的使用,要同类型变量
        print(str(j)+'*'+str(i)+'='+str(i*j),end='\t')
    print('')
```



## 四 数据类型

Python3 中常见的数据类型有：

- Number（数字）
- String（字符串）
- bool（布尔类型）
- List（列表）
- Tuple（元组）
- Set（集合）
- Dictionary（字典）

Python3 的六个**标准数据类型**中：

- **不可变**数据（3 个）：Number（数字）、String（字符串）、Tuple（元组）；
- 可变数据（3 个）：List（列表）、Dictionary（字典）、Set（集合）。

此外还有一些高级的数据类型，如: 字节数组类型(bytes)。

### 0 序列



![屏幕截图 2024-05-01 135401](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20135401-1714543921063-5-1714557083288-71.png)



![屏幕截图 2024-05-01 140238](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20140238-1714543940614-10.png)

![屏幕截图 2024-05-01 140549](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20140549-1714543950557-13.png)

```
# 逆序输出
s='helloworld'
print(s[::-1])
```



### 1 Number(数字)

Python 支持三种不同的数值类型：

- **整型(int)** - 通常被称为是整型或整数，是正或负整数，**不带小数点**。Python3 整型是没有限制大小的，可以当作 Long 类型使用，所以 Python3 没有 Python2 的 Long 类型。布尔(bool)是整型的子类型。
- **浮点型(float)** - 浮点型由整数部分与小数部分组成，浮点型也可以使用科学计数法表示（2.5e2 = 2.5 x 102 = 250）
- **复数( (complex))** - 复数由实数部分和虚数部分构成，可以用a + bj,或者complex(a,b)表示， 复数的实部a和虚部b都是浮点型。

#### 1 数学函数

| 函数           | 返回值 ( 描述 )                                              |
| -------------- | ------------------------------------------------------------ |
| abs(x)         | 返回数字的绝对值，如abs(-10) 返回 10                         |
| ceil(x)        | 返回数字的**上入整数**，如math.ceil(4.1) 返回 5              |
| cmp(x, y)      | 如果 x < y 返回 -1, 如果 x == y 返回 0, 如果 x > y 返回 1。 **Python 3 已废弃，使用 (x>y)-(x<y) 替换**。 |
| exp(x)         | 返回e的x次幂(ex),如math.exp(1) 返回2.718281828459045         |
| fabs(x)        | 以浮点数形式返回数字的**绝对值**，如math.fabs(-10) 返回10.0  |
| floor(x)       | 返回数字的**下舍整数**，如math.floor(4.9)返回 4              |
| **log**(x)     | 如math.log(math.e)返回1.0,math.log(100,10)返回2.0            |
| **log**10(x)   | 返回以10为基数的x的对数，如math.log10(100)返回 2.0           |
| max(x1, x2,…)  | 返回给定参数的**最大值**，参数可以为序列。                   |
| min(x1, x2,…)  | 返回给定参数的**最小值**，参数可以为序列。                   |
| modf(x)        | 返回x的小数部分与整数部分，整数部分以浮点型表示。(0.12000000000000455, 100.0) |
| pow(x, y)      | x**y 运算后的值。                                            |
| \round(x [,n]) | 返回浮点数 x 的四舍五入值，如给出 n 值，则代表舍入到小数点后的位数。**其实准确的说是保留值将保留到离上一位   *更近*   的一端。** |
| sqrt(x)        | 返回数字x的**平方根**。                                      |

------

#### 2 随机数函数

随机数可以用于数学，游戏，安全等领域中，还经常被嵌入到算法中，用以提高算法效率，并提高程序的安全性。

Python包含以下常用随机数函数：

| 函数                             | 描述                                                         |
| -------------------------------- | ------------------------------------------------------------ |
| choice(seq)                      | 从**序列**的元素中随机挑选一个元素，比如random.choice(range(**10**))，从**0到9**中随机挑选一个**整数**。 |
| \randrange ([start,\stop ,step]) | 从指定范围内，按指定**基数递增**的集合中获取一个随机数，基数默认值为 1 |
| random()                         | 随机生成**下一个实数**，它在**[0,1)**范围内。                |
| \seed([x])                       | 改变随机数生成器的**种子**seed。如果你不了解其**原理**，你不必特别去设定seed，Python会帮你选择seed。 |
| shuffle(lst)                     | 将序列的所有元素**随机排序**                                 |
| uniform(x, y)                    | **随机生成下一个实数**，它在**[x,y]**范围内。                |

------

#### 3 三角函数

Python包括以下三角函数：

| 函数        | 描述                                              |
| ----------- | ------------------------------------------------- |
| acos(x)     | 返回x的反余弦弧度值。                             |
| asin(x)     | 返回x的反正弦弧度值。                             |
| atan(x)     | 返回x的反正切弧度值。                             |
| atan2(y, x) | 返回给定的 X 及 Y 坐标值的反正切值。              |
| cos(x)      | 返回x的弧度的余弦值。                             |
| hypot(x, y) | 返回欧几里德范数 sqrt(x_x + y_y)。                |
| sin(x)      | 返回的x弧度的正弦值。                             |
| tan(x)      | 返回x弧度的正切值。                               |
| degrees(x)  | 将弧度转换为角度,如degrees(math.pi/2) ， 返回90.0 |
| radians(x)  | 将角度转换为弧度                                  |

------

#### 4 数学常量

| 常量   | 描述                                  |
| ------ | ------------------------------------- |
| **pi** | 数学常量 pi（圆周率，一般以π来表示）  |
| **e**  | 数学常量 e，e即自然常数（自然常数）。 |

### 2 List（列表）

序列的一种

![屏幕截图 2024-05-01 141844](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20141844-1714545005247-16.png)



#### 列表的创建和遍历：

##### 	遍历列表的三种方式：

![屏幕截图 2024-05-01 141932](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20141932-1714545015309-19.png)

```
lst1=['hello', 'world', 'python', 'mpf']
lst2=list('hello'+'world')
# 遍历列表的三种方式
# 一 for循环遍历
for item in lst1:
    print(item)
# 二 通过索引遍历
for i in range(0,len(lst1)):
    print(i,'-->',lst1[i])
# 三 通过enumerate遍历
for index, item in enumerate (lst1):
    print(index,item)  # index是序号，不是索引
# 可以手动修改
for i, item in enumerate(lst1,start=1):
     print(i,item)
# hello
# world
# python
# mpf
# 0 --> hello
# 1 --> world
# 2 --> python
# 3 --> mpf
# 0 hello
# 1 world
# 2 python
# 3 mpf
# 1 hello
# 2 world
# 3 python
# 4 mpf
```



#### 列表的特殊操作：



![屏幕截图 2024-05-01 144528](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20144528-1714546548565-25.png)



**排序：**

![屏幕截图 2024-05-01 145101](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20145101-1714546502946-22.png)

```
lst=[10,20,56,3,89,0]
lst1=lst.copy()
lst.sort()  # 默认升序
print(lst)
lst.sort(reverse= True)
print(lst)
new_lst=sorted(lst1)  # 相当于排序副本，不会改变原序列
print(lst1)
print(new_lst)
```



**列表生成式：**

![屏幕截图 2024-05-01 152237](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20152237-1714548186327-28.png)

```
#  列表生成式：4行5列二维列表
lst = [[j for j in range(5)] for i in range(4)]
#  二维列表遍历
for row in lst:
    for i in row:
        print(i,end='\t')
    print('')
# 0 1  2  3  4  
# 0 1  2  3  4  
# 0 1  2  3  4  
# 0 1  2  3  4
```



### 3 Tuple（元组）

![屏幕截图 2024-05-01 153651](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20153651-1714549481665-31.png)

```
t = ('hello',[10,3,56],'python','mpf')
print(t)
t1=tuple('hello')
print(t1)  # 把每个字母当作tuple中的元素
t=tuple([10,20,'hello','world'])
print(t)  # 把每个序列元素当作tuple中的元素
# ('hello', [10, 3, 56], 'python', 'mpf')
# ('h', 'e', 'l', 'l', 'o')
# (10, 20, 'hello', 'world')
print('-'*20)
t2=(20)  # 只有一个元素时省略, 则不是元组类型
print(t2,type(t2))
t2=(20,)
print(t2,type(t2))
# --------------------
# 20 <class 'int'>
# (20,) <class 'tuple'>
```



#### 元组与列表的区别

![屏幕截图 2024-05-01 160707](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20160707-1714550904253-39.png)



### 4 Dictionary（字典）





![屏幕截图 2024-05-01 161141](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20161141-1714554786191-42.png)



![屏幕截图 2024-05-01 171008](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20171008-1714554801027-45.png)

```
d={'hello':10,'world':20,'python':30}
#  访问字典中的元素
#  (1)使用d[key]
print(d['hello'])
#  (2)使用d.get(key)
print(d.get('hello'))
#  二者之间的区别在于，d[key]在遇到没有key的时候会报错，但是d.[key]会输出默认值
#  print(d['java']) #  KeyError； ’java‘
print(d.get('java'))  #  None
print(d.get('java','不存在'))  #  不存在

#  字典的遍历
for item in d.items():
    print(item) #  元组的形式
for key,value in d.items():
    print(key,value)
```





![屏幕截图 2024-05-01 172311](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20172311-1714555617146-48.png)



![屏幕截图 2024-05-01 172506](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20172506-1714555635868-51.png)



### 5 Set（集合）（无序）



![屏幕截图 2024-05-01 172743](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20172743-1714556409315-54.png)

![屏幕截图 2024-05-01 172807](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20172807-1714556421236-57.png)

```
#  {}直接创建集合
s={10,20,30,40}
print(s)  # {40, 10, 20, 30}
#  集合只能存储不可变数据类型
# s={[10,20],[30,40]} #TypeError: unhashable type: 'list'

#  使用set()创建集合
s=set()
print(s)
s={}  # 创建的是一个字典
s1=set('helloworld')
print(s1)  # 无序不重复：{'w', 'e', 'o', 'h', 'r', 'l', 'd'}
```



![屏幕截图 2024-05-01 173757](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20173757-1714556445731-60.png)



![屏幕截图 2024-05-01 173920](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20173920-1714556454833-63.png)

### 6 Python数据类型转换

有时候，我们需要对数据内置的类型进行转换，数据类型的转换，你只需要将数据类型作为函数名即可，在下一章节 Python3 数据类型转换 会具体介绍。

以下几个内置的函数可以执行数据类型之间的转换。这些函数返回一个新的对象，表示转换的值。

| 函数                  | 描述                                                         |
| --------------------- | ------------------------------------------------------------ |
| [int(x ,base])        | 将x转换为一个整数                                            |
| float(x)              | 将x转换到一个浮点数                                          |
| [complex(real ,imag]) | 创建一个复数                                                 |
| str(x)                | 将对象 x 转换为字符串                                        |
| repr(x)               | 将对象 x 转换为表达式字符串*********                         |
| eval(str)             | 用来计算在字符串中的有效Python表达式,并返回一个对象********* |
| tuple(s)              | 将序列 s 转换为一个元组                                      |
| list(s)               | 将序列 s 转换为一个列表                                      |
| set(s)                | 转换为可变集合                                               |
| dict(d)               | 创建一个字典。d 必须是一个 (key, value)元组序列。            |
| frozenset(s)          | 转换为不可变集合***                                          |
| chr(x)                | 将一个整数转换为一个字符***                                  |
| ord(x)                | 将一个字符转换为它的整数值***                                |
| hex(x)                | 将一个整数转换为一个十六进制字符串***                        |
| oct(x)                | 将一个整数转换为一个八进制字符串***                          |

### 7 数据组合类型总结：



![屏幕截图 2024-05-01 174940](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20174940-1714557039328-66.png)

![屏幕截图 2024-05-01 174951](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-01%20174951-1714557051679-69.png)



### 代码实战2：

```
#  模拟京东购物流程
#  商品信息列表
lst=[]
for i in range(5):
    item = input('请输入要添加的商品信息：')
    lst.append(item)
#输出列表中商品
print('商品信息：')
for item in lst:
    print(item)
#  购物车商品列表
goods=[]
while True:
    flag = False
    num = input('请输入商品编号：')
    for item in lst:
        if num == item[0:4]:  # 切片去匹配编号
            flag = True
            goods.append(item)
            print('商品已添加进购物车')
            break
    if flag == False and num != 'q':
        print('没有该件商品！')
    if num == 'q':
        break
print('您选择的商品为：')
goods.reverse()
print(goods)
```

```
#  12306铁路票务系统
dict_ticket = {
    'G1569': ['北京-天津南', '18:06', '18:39', '00:33'],
    'G1355': ['北京-天津', '18:00', '18:29', '00:29'],
    'G1869': ['北京-天津西', '18:12', '18:36', '00:24'],
    'G1239': ['北京-天津北', '19:06', '19:39', '00:33']
}
print('车次   出发站-到达站     出发时间    到达时间    历时时长')
#  遍历字典中的元素
for key in dict_ticket.keys():
    print(key, end=' ')  # 获取key值，和value列表print在同一行
#  根据key值遍历value列表
    for item in dict_ticket.get(key):
        print(item, end='\t\t')
    print()

#  输入用户的购票车次
train_no = input('请输入要购买的车次：')
#  根据key获取值,info为列表
info = dict_ticket.get(train_no,'车次不存在')
#  判断车次是否存在
if info != '车次不存在':
    person = input('请输入乘车人，如果是多位逗号隔开：')
    #  获取车次出发站-到达站，出发时间
    s=info[0]+' '+info[1]+'开'
    print('您已经购买了'+train_no+' '+s+',请'+person+'注意乘车时间。【12306铁路客服】')
```



### 8 String（字符串）

#### 1 Python 转义字符

在需要在字符中使用特殊字符时，python 用反斜杠 **** 转义字符。如下表：

| 转义字符   | 描述                                                         | 实例                                                         |
| ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| (在行尾时) | **续行符**                                                   | `>>> print("line1 \ ... line2 \ ... line3") line1 line2 line3 >>>` |
| \          | 反斜杠符号                                                   | `>>> print("\\") \`                                          |
| ’          | 单引号                                                       | `>>> print('\'') '`                                          |
| "          | 双引号                                                       | `>>> print("\"") "`                                          |
| \a         | **响铃**                                                     | `>>> print("\a")`执行后电脑有响声。                          |
| \b         | 退格(Backspace)                                              | `>>> print("Hello \b World!") Hello World!`                  |
| \000       | **空**                                                       | `>>> print("\000") >>>`                                      |
| \n         | 换行                                                         | `>>> print("\n") >>>`                                        |
| \v         | 纵向制表符                                                   | `>>> print("Hello \v World!") Hello World! >>>`              |
| \t         | 横向制表符                                                   | `>>> print("Hello \t World!") Hello World! >>>`              |
| \r         | 回车，将 **\r** 后面的内容移到字符串**开头**，并**逐一替换**开头部分的字符，**直至**将 **\r** 后面的内容**完全替换完成**。 | `>>> print("Hello\rWorld!") World! >>> print('google runoob taobao\r123456') 123456 runoob taobao` |
| \f         | **换页**                                                     | `>>> print("Hello \f World!") Hello World! >>>`              |
| \yyy       | **八进制数**，y 代表 0~7 的字符，例如：\012 代表换行。       | `>>> print("\110\145\154\154\157\40\127\157\162\154\144\41") Hello World!` |
| \xyy       | **十六进制数**，以 \x 开头，y 代表的字符，例如：\x0a 代表换行 | `>>> print("\x48\x65\x6c\x6c\x6f\x20\x57\x6f\x72\x6c\x64\x21") Hello World!` |
| \other     | 其它的字符以普通格式输出                                     |                                                              |

#### 2 Python 字符串运算符

下表实例变量 a 值为字符串 “Hello”，b 变量值为 “Python”：

| 操作符 | 描述                                                         | 实例                            |
| ------ | ------------------------------------------------------------ | ------------------------------- |
| +      | 字符串连接                                                   | a + b 输出结果： HelloPython    |
| *      | 重复输出字符串                                               | a*2 输出结果：HelloHello        |
| []     | 通过**索引**获取字符串中字符                                 | a[1] 输出结果 **e**             |
| [ : ]  | 截取字符串中的一部分，遵循**左闭右开**原则，str[0:2] 是不包含第 3 个字符的。 | a[1:4] 输出结果 **ell**         |
| in     | **成员运算符** - 如果字符串中包含给定的字符返回 True         | **‘H’ in a** 输出结果 True      |
| not in | 成员运算符 - 如果字符串中不包含给定的字符返回 True           | **‘M’ not in a** 输出结果 True  |
| r/R    | 原始字符串 - 原始字符串：所有的字符串都是**直接按照字面的意思来使用**，没有转义特殊或不能打印的字符。 原始字符串除在字符串的**第一个引号前加上字母 r**（可以大小写）以外，与普通字符串有着几乎完全相同的语法。 | `print( r'\n' ) print( R'\n' )` |
| %      | 格式字符串                                                   | 请看下一节内容。                |

#### 3 Python 字符串格式化

Python 支持**格式化字符串**的输出 。尽管这样可能会用到非常复杂的表达式，但最基本的用法是将一个值插入到一个有字符串格式符 %s 的字符串中。

在 Python 中，字符串格式化使用与 C 中 sprintf 函数一样的语法。

```
  print ("我叫 %s 今年 %d 岁!" % ('小明', 10))
```

以上实例输出结果：

```
我叫 小明 今年 10 岁!
```

python字符串格式化符号:

| 符 号  | 描述                                         |
| ------ | -------------------------------------------- |
| %c     | 格式化**字符**及其**ASCII码**                |
| %s     | 格式化**字符串**                             |
| %d     | 格式化**整数**                               |
| %u     | 格式化**无符号整型**                         |
| %o     | 格式化**无符号八进制数**                     |
| %x     | 格式化**无符号十六进制数**                   |
| %**X** | 格式化**无符号十六进制数（大写）**           |
| %f     | 格式化**浮点数字**，可指定小数点后的**精度** |
| %e     | 用**科学计数法**格式化浮点数                 |
| %E     | 作用**同**%e，用科学计数法格式化浮点数       |
| %g     | %f和%e的**简写**                             |
| %G     | %f 和 %E 的**简写**                          |
| %p     | 用十六进制数格式化变量的**地址*****          |

格式化操作符辅助指令:

| 符号      | 功能                                                         |
| --------- | ------------------------------------------------------------ |
| *         | 定义**宽度**或者小数点**精度**                               |
| -         | 用做**左对齐**                                               |
| +         | 在正数前面**显示加号**( + )                                  |
|           | 在正数前面显示空格                                           |
| #         | 在八进制数前面**显示零**(‘0’)，在十六进制前面**显示’0x’或者’0X’**(取决于用的是’x’还是’X’) |
| 0         | 显示的数字前面**填充’0’**而不是默认的空格                    |
| %         | ‘%%‘输出一个**单一的’%’**                                    |
| **(var)** | **映射变量(字典参数，键)**                                   |
| m.n.      | m 是显示的**最小总宽度**,n 是**小数点后的位数**(如果可用的话) |

Python2.6 开始，新增了一种格式化字符串的函数 **str.format()**，它增强了字符串格式化的功能。

#### 4 f-string

**f-string** 是 python3.6 之后版本添加的，称之为**字面量**格式化字符串，是新的格式化字符串的语法。

之前我们习惯用百分号 (%):

例如

```
name = 'wcm'
print('Hello %s' % name) #Hello wcm
or
print("hello "+name)   #Hello wcm
```

现在我们可以用更简单的f

```
name = 'wcm'
print (f "hello {name}")  #Hello wcm  替换变量
print(f'{1+2}')           # 使用表达式
```

### 

![屏幕截图 2024-05-03 155643](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-03%20155643-1714723084125-2.png)

![image-20240503160132992](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/image-20240503160132992-1714723295078-4.png)

#### 5.格式化字符串：



![image-20240503160259657](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/image-20240503160259657-1714723381535-6.png)

```
name = '马鹏飞'
age = 18
score = 98.5
#  (1)占位符
print('姓名：%s,年龄: %d,成绩：%.1f' % (name, age, score))
#  (2)f-string
print(f'姓名: {name},年龄：{age},成绩：{score}')
#  (3）使用字符串的format方法
print('姓名：{0},年龄：{1},成绩：{2}'.format(name,age,score) )
#  下标序号一一对应,同上
print('姓名：{1},年龄：{2},成绩：{0}'.format(score,name,age) )
# 姓名：马鹏飞,年龄: 18,成绩：98.5
# 姓名: 马鹏飞,年龄：18,成绩：98.5
# 姓名：马鹏飞,年龄：18,成绩：98.5
# 姓名：马鹏飞,年龄：18,成绩：98.5
```

![屏幕截图 2024-05-03 162528](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-03%20162528-1714725004576-9.png)

#### 6.字符串的编码与解码：

![屏幕截图 2024-05-03 162704](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-03%20162704-1714725029150-12.png)

![屏幕截图 2024-05-03 162656](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-05-03%20162656-1714725043823-17.png)



```
注意：
	strict：编码找不到时报错
	ignore：编码找不到时忽略
	replace：编码找不到时用？替换
```





#### 7.数据验证：

![image-20240503163450748](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/image-20240503163450748-1714725292096-19.png)



![image-20240503163520333](./Python%20%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%EF%BC%9A.assets/image-20240503163520333-1714725321360-21.png)

```
s1='hello'
s2='world'
# (1)+拼接
print(s1+s2)
#  (2)字符串的join方法
print(''.join([s1,s2]))  # 直接连接
print('*'.join([s1,s2]))  # 用*连接
#  (3)直接拼接
print('hello''world')
#  (4)格式化字符串连接
print('%s%s' % (s1,s2))
print(f'{s1}{s2}')
print('{0}{1}'.format(s1,s2))
```





## 五 函数

## 定义一个函数

你可以定义一个由自己想要功能的函数，以下是简单的规则：

- 函数代码块以 **def** 关键词开头，后接函数标识符名称和圆括号**()**。
- 任何传入参数和自变量必须放在圆括号中间。圆括号之间可以用于定义参数。
- 函数的第一行语句可以选择性地使用文档字符串—用于存放函数说明。
- 函数内容以冒号起始，并且缩进。
- **return [表达式]** 结束函数，选择性地返回一个值给调用方。不带表达式的return相当于返回 None。

------

### 语法

```
def functionname( parameters ):
   "函数_文档字符串"
   function_suite
   return [expression]
```

默认情况下，参数值和参数名称是按函数声明中定义的顺序匹配起来的。

## 参数传递

```
在 python 中，类型属于对象，变量是没有类型的：

a=[1,2,3] 
a="Runoob"
```

以上代码中，**[1,2,3]** 是 List 类型，**"Runoob"** 是 String 类型，而变量 a 是没有类型，她仅仅是一个对象的引用（一个指针），可以是 List 类型对象，也可以指向 String 类型对象。

### 可更改(mutable)与不可更改(immutable)对象

在 python 中，strings, tuples, 和 numbers 是不可更改的对象，而 list,dict 等则是可以修改的对象。

- **不可变类型：**变量赋值 **a=5** 后再赋值 **a=10**，这里实际是新生成一个 int 值对象 10，再让 a 指向它，而 5 被丢弃，不是改变a的值，相当于新生成了a。
- **可变类型：**变量赋值 **la=[1,2,3,4]** 后再赋值 **la[2]=5** 则是将 list la 的第三个元素值更改，本身la没有动，只是其内部的一部分值被修改了。

python 函数的参数传递：

- **不可变类型：**类似 c++ 的值传递，如 整数、字符串、元组。如fun（a），传递的只是a的值，没有影响a对象本身。比如在 fun（a）内部修改 a 的值，只是修改另一个复制的对象，不会影响 a 本身。
- **可变类型：**类似 c++ 的引用传递，如 列表，字典。如 fun（la），则是将 la 真正的传过去，修改后fun外部的la也会受影响

python 中一切都是对象，严格意义我们不能说值传递还是引用传递，我们应该说传不可变对象和传可变对象。

### python 传不可变对象实例

```
#!/usr/bin/python 
# -*- coding: UTF-8 -*-  

def ChangeInt( a ):    
	a = 10  
b = 2 
ChangeInt(b) 
print b # 结果是 2
```

实例中有 int 对象 2，指向它的变量是 b，在传递给 ChangeInt 函数时，按传值的方式复制了变量 b，a 和 b 都指向了同一个 Int 对象，在 a=10 时，则新生成一个 int 值对象 10，并让 a 指向它。

### 传可变对象实例

```
#!/usr/bin/python
# -*- coding: UTF-8 -*-
 
# 可写函数说明
def changeme( mylist ):
   "修改传入的列表"
   mylist.append([1,2,3,4])
   print "函数内取值: ", mylist
   return
 
# 调用changeme函数
mylist = [10,20,30]
changeme( mylist )
print "函数外取值: ", mylist
```

实例中传入函数的和在末尾添加新内容的对象用的是同一个引用，故输出结果如下：

```
函数内取值:  [10, 20, 30, [1, 2, 3, 4]]
函数外取值:  [10, 20, 30, [1, 2, 3, 4]]
```
