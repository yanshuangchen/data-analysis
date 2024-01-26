# python基础
本片文章参考[菜鸟教程](https://www.runoob.com/python/python-variable-types.html)
## 一些概念
---
### 解释型语言
没有编译环节
### 交互式语言
可以在`>>>`后直接执行代码
### 面向对象语言
风格或者代码封装在对象
### IDE
就是集成开发环境的意思
### 编码
python默认编码为ASCII模式，打印汉字时可能需要加入utf-8
### 字符串输入
    s='abcdef'
    s[1:5]
    'bcde'
    s[1]=b
    s[5]=f
实例   

    str = 'Hello World!'
    print str
    print str[0]
    print str[2:5]
    print str[2:]
    print str * 2
    print str + "TEST"     

以上的结果是

    Hello World!
    H
    llo
    llo World!
    Hello World!Hello World!
    Hello World!TEST
 ### 列表
实例

    list = [ 'runoob', 786 , 2.23, 'john', 70.2 ]
    tinylist = [123, 'john']
    
    print list               # 输出完整列表
    print list[0]            # 输出列表的第一个元素
    print list[1:3]          # 输出第二个至第三个元素 
    print list[2:]           # 输出从第三个开始至列表末尾的所有元素
    print tinylist * 2       # 输出列表两次
    print list + tinylist    # 打印组合的列表
以上实例的输出结果

    ['runoob', 786, 2.23, 'john', 70.2]
    runoob
    [786, 2.23]
    [2.23, 'john', 70.2]
    [123, 'john', 123, 'john']
    ['runoob', 786, 2.23, 'john', 70.2, 123, 'john']
### 元组
使用`()`来进行标识。内部元素用逗号隔开。元组不能进行二次赋值，相当于只读列表。  
实例

    #!/usr/bin/python
    # -*- coding: UTF-8 -*-

    tuple = ( 'runoob', 786 , 2.23, 'john', 70.2 )
    tinytuple = (123, 'john')
    
    print tuple               # 输出完整元组
    print tuple[0]            # 输出元组的第一个元素
    print tuple[1:3]          # 输出第二个至第四个（不包含）的元素 
    print tuple[2:]           # 输出从第三个开始至列表末尾的所有元素
    print tinytuple * 2       # 输出元组两次
    print tuple + tinytuple   # 打印组合的元组
输出同列表相同，但是更新数值的操作对于元组来说是非法的。

### 字典
相比于列表，字典是无序的对象集合。  
字典中的元素是通过键来存取的，而不是通过偏移存取。  
字典由索引`key`和对应的值`value`组成。  
实例

    #!/usr/bin/python
    # -*- coding: UTF-8 -*-
    
    dict = {}
    dict['one'] = "This is one"
    dict[2] = "This is two"
    
    tinydict = {'name': 'runoob','code':6734, 'dept': 'sales'}
    
    
    print dict['one']          # 输出键为'one' 的值
    print dict[2]              # 输出键为 2 的值
    print tinydict             # 输出完整的字典
    print tinydict.keys()      # 输出所有键
    print tinydict.values()    # 输出所有值

输出结果为

    This is one
    This is two
    {'dept': 'sales', 'code': 6734, 'name': 'runoob'}
    ['dept', 'code', 'name']
    ['sales', 6734, 'runoob']
### 进行python数据的转换
    int(x [,base])

    将x转换为一个整数

    long(x [,base] )

    将x转换为一个长整数

    float(x)

    将x转换到一个浮点数

    complex(real [,imag])

    创建一个复数

    str(x)

    将对象 x 转换为字符串

    repr(x)

    将对象 x 转换为表达式字符串

    eval(str)

    用来计算在字符串中的有效Python表达式,并返回一个对象

    tuple(s)

    将序列 s 转换为一个元组

    list(s)

    将序列 s 转换为一个列表

    set(s)

    转换为可变集合

    dict(d)

    创建一个字典。d 必须是一个序列 (key,value)元组。

    frozenset(s)

    转换为不可变集合

    chr(x)

    将一个整数转换为一个字符

    unichr(x)

    将一个整数转换为Unicode字符

    ord(x)

    将一个字符转换为它的整数值

    hex(x)

    将一个整数转换为一个十六进制字符串

    oct(x)

    将一个整数转换为一个八进制字符串

### 算数运算符
`%`代表求mod的意思，`**`代表幂的意思
#### 位运算符
    #!/usr/bin/python
    # -*- coding: UTF-8 -*-
    
    a = 60            # 60 = 0011 1100 
    b = 13            # 13 = 0000 1101 
    c = 0
    
    c = a & b;        # 12 = 0000 1100
    print "1 - c 的值为：", c
    
    c = a | b;        # 61 = 0011 1101 
    print "2 - c 的值为：", c
    
    c = a ^ b;        # 49 = 0011 0001
    print "3 - c 的值为：", c
    
    c = ~a;           # -61 = 1100 0011
    print "4 - c 的值为：", c
    
    c = a << 2;       # 240 = 1111 0000
    print "5 - c 的值为：", c
    
    c = a >> 2;       # 15 = 0000 1111
    print "6 - c 的值为：", c
### 逻辑运算符
`and` `not` `or`
代表了与或非，会返回布尔值

### 成员运算符
`in` `not in`代表了一个变量是否在指定的列表和元组中，然后返回的是bool值
### 通过序列索引迭代
    #!/usr/bin/python
    # -*- coding: UTF-8 -*-
    
    fruits = ['banana', 'apple',  'mango']
    for index in range(len(fruits)):
    print ('当前水果 : %s' % fruits[index])
    
    print ("Good bye!")
### 查看库中的函数
例如`dir(math)`
### 字符串的截取
    #!/usr/bin/python
    
    var1 = 'Hello World!'
    var2 = "Python Runoob"
    
    print "var1[0]: ", var1[0]
    print "var2[1:5]: ", var2[1:5]
字符串的连接使用加号来进行 
### 列表
#### 更新列表
    #!/usr/bin/python
    # -*- coding: UTF-8 -*-
    
    list = []          ## 空列表
    list.append('Google')   ## 使用 append() 添加元素
    list.append('Runoob')
    print list

#### 删除列表元素
    #!/usr/bin/python
    
    list1 = ['physics', 'chemistry', 1997, 2000]
    
    print list1
    del list1[2]
    print "After deleting value at index 2 : "
    print list1
#### 测量长度
`len`
#### 列表截取
`L[-2]`代表列表中倒数第二个元素
#### 一些方法
    1   list.append(obj)
    在列表末尾添加新的对象
    2	list.count(obj)
    统计某个元素在列表中出现的次数
    3	list.extend(seq)
    在列表末尾一次性追加另一个序列中的多个值（用新列表扩展原来的列表）
    4	list.index(obj)
    从列表中找出某个值第一个匹配项的索引位置
    5	list.insert(index, obj)
    将对象插入列表
    6	list.pop([index=-1])
    移除列表中的一个元素（默认最后一个元素），并且返回该元素的值
    7	list.remove(obj)
    移除列表中某个值的第一个匹配项
    8	list.reverse()
    反向列表中元素
    9	list.sort(cmp=None, key=None, reverse=False)
    对原列表进行排序
### 格式化日期
    #!/usr/bin/python
    # -*- coding: UTF-8 -*-
    
    import time
    
    # 格式化成2016-03-20 11:45:39形式
    print time.strftime("%Y-%m-%d %H:%M:%S", time.localtime()) 
    
    # 格式化成Sat Mar 28 22:24:24 2016形式
    print time.strftime("%a %b %d %H:%M:%S %Y", time.localtime()) 
    
    # 将格式字符串转换为时间戳
    a = "Sat Mar 28 22:24:24 2016"
    print time.mktime(time.strptime(a,"%a %b %d %H:%M:%S %Y")) 
一些使用方法

    python中时间日期格式化符号：

    %y 两位数的年份表示（00-99）
    %Y 四位数的年份表示（000-9999）
    %m 月份（01-12）
    %d 月内中的一天（0-31）
    %H 24小时制小时数（0-23）
    %I 12小时制小时数（01-12）
    %M 分钟数（00-59）
    %S 秒（00-59）
    %a 本地简化星期名称
    %A 本地完整星期名称
    %b 本地简化的月份名称
    %B 本地完整的月份名称
    %c 本地相应的日期表示和时间表示
    %j 年内的一天（001-366）
    %p 本地A.M.或P.M.的等价符
    %U 一年中的星期数（00-53）星期天为星期的开始
    %w 星期（0-6），星期天为星期的开始
    %W 一年中的星期数（00-53）星期一为星期的开始
    %x 本地相应的日期表示
    %X 本地相应的时间表示
    %Z 当前时区的名称
    %% %号本身
