## 类型

`int`:

`float`:

`complex`:

`bool`:

`str`:

`List`:

`Tuple`:

`Set`:

`Dictionary`:



## 字符串

``` python
# 单引号
name = 'xxx'
# 双引号
name = "xxx"
# 三引号
name = """xxx"""
```

* 参考javascript



## 注释

``` python
# xxxx

"""
	xxxxxxx
"""
```



## 类型

> 查看类型

``` python
type(x)
```

> 类型转换

``` python
int(x)
float(x)
str(x)
```



## 运算符

`+` `-` `*` `\` ：加减乘除

`//`: 取整除 9 // 2 = 4

`%`： 取余  9 % 2 = 1

`**`:  指数 例如：2`**`2 = 4  3`**`2  = 9  

`=`：赋值

`+=` `-=` `*=` `/=` `%=` `**=` `//=`



## if

``` python
if 条件:
    #方法体
```



## if else

``` python
if 条件：
	xxx
else: 
    xxx
```



## if elif  else

``` python
if 条件1：
	#方法体
elif 条件2:
   	#方法体
else:
   	#方法体
```



## while

``` python
while 条件:
	# 方法体
```



## for 

``` python
name = "465487"
for x in name:
	#方法体
```

* break 结束循环
* continue 跳过下面的代码，进入下一次循环



## range

``` python
range(5) # [0,5) =  [0,1,2,3,4]
range(5,10) # [5,10) = [5,6,7,8,9]

step = 2 # 步长
range(5,10, step) # [5,10) 范围步长2 = [5,7,9] 
```



## 函数

``` python
x = 10  # 全局变量 x

def my_function(param1, param2):
    """
    这里可以提供关于函数的详细描述、参数的解释、返回值说明等等。

    参数:
    param1 (类型): 参数1的描述
    param2 (类型): 参数2的描述

    返回:
    返回值的类型: 返回值的描述
    """
    # 函数的实际代码
    
    global x  # 使用 global 关键字声明 x 是全局变量
    x = 20     # 修改全局变量 x 的值
    return

none_return = my_function("param1", "param2")
print(none_return) # NoneType
print(type(none_return)) # <class 'NoneType'>
print(x)  # 打印全局变量 x，输出为 20
```

* None：空的 = False; 函数没有使用return返回`None`;  type <class 'NoneType'>
* 局部变量：在函数体内部，临时保存数据，函数调用完成后，则销毁局部变量
* 全局变量：在函数体内、外都能生效的变量
* global关键字：函数内部为全局变量重新赋值。
* 说明文档："""  """



## 列表 List

* `有序` `可重复` `可修改` `混装` 
*  创建： `[]`  分隔：`,` 

``` python
my_list = [1, 2, 3, 'apple', 'banana']
```







### 操作

``` python
my_list = [1, 2, 3, 'apple', 'banana']

""" 查询 """
# 下标访问
first_element = my_list[0]  # 访问第一个元素，值为1
# 倒叙下标访问
last_element = my_list[-1]  # 访问最后一个元素，值为'banana'

""" 插入 """
# 下标插入
my_list.insert(1, "itheima")
# 尾部追加
my_list.append(4)
# 尾部追加其他容器
my_list.extend([4,5,6]) 

""" 删除 """
# 下标删除
del my_list[0]
my_list.pop(0)
# 删除某元素在列表中的第一个匹配项
my_list.remove('apple')
# 清空
my_list.clear()

""" 统计数量 """
# 统计某元素在列表内的数量
my_list.count('banana')
# 统计列表内有多少元素
len(my_list)


""" 切片 """
subset = my_list[1:4]  # 切片 获取索引1到3的元素，结果为[2, 3, 'apple']
```





## 集合 Sets

* `无序` `不重复` `可修改` `混装`
*  创建：`{}` 分隔：`,` 

``` python
my_set = {1, 2, 3, 4, 5}
```



### 操作

``` python
my_set: set[str] = {"hello", "world"}

# 添加新元素
my_set.add("wjq")  # {'world', 'hello', 'wjq'} {'wjq', 'world', 'hello'}

# 移除指定元素
my_set.remove("hello")  # {'world', 'wjq'} {'wjq', 'world'}

# 从集合中随机取出一个元素
element = my_set.pop()  # world wjq

# 清空
my_set.clear()  # set()

# 取出2个集合的差集
set1 = {1, 2, 3}
set2 = {1, 5, 6}
set3 = set1.difference(set2) # {2, 3}

# 消除2个集合的差集
set1 = {1, 2, 3}
set2 = {1, 5, 6}
set1.difference_update(set2)
print(set1) # {2, 3}
print(set2) #{1, 5, 6}

# 并集
set1 = {1, 2, 3}
set2 = {1, 5, 6}
set3 = set1.union(set2) #  set3 {1, 2, 3, 5, 6}
```







## 元组 Tuples

* `有序` `可重复` `不可修改` `混装`
*  创建：`()` 分隔：`,` 

``` python
my_tuple = (1, 2, 3, 'apple', 'banana')
```



### 操作

``` python
""" 查询 """
# 下标查询
my_tuple.[0]
my_tuple.index(1)

""" 统计数量 """
# 统计某元素在列表内的数量
my_tuple.count('banana')
# 统计列表内有多少元素
len(my_tuple)

```



## 字典 Dictionaries

* `无序` `可变` `键-值对`
* 创建:`{}` ，键和值 `:` 分隔，键-值对 `,` 分隔

``` python
my_dict = {'name': 'John', 'age': 30, 'city': 'New York'}
```







## 字符串 String

* `有序` `不可修改` 
* 创建: `' '`、双引号 `" "` 或三重引号 `''' '''`

``` python
my_string = "Hello, World!"
```



### 操作

``` python
""" 查询 """
# 下标获取指定位置的字符
my_string[0] # 结果 H
my_string[-1] # 结果 !

# 查找特定字符串位置的下标索引值
my_string.index("Wor") # 结果7

# 空格分割
string_list = my_string.split(" ")  # 结果 ['Hello', 'World']

# 字符串的规整操作（去前后空格）
my_str = " !hello world! "
my_str = my_str.strip() # 结果 "!hello world!"

# 去除指定字符串
my_str = my_str.strip("!")  # 结果 "hello world"

# 统计字符串内字符串的出现次数
o_count = my_str.count("o") # 结果 2

# 统计字符串的字符个数
str_len = len(my_str) # 结果 11
```



## 序列

* `内容连续` `有序` `下标访问`
* `列表` `元组` `字符串` 



## 切片

* `序列` 
* 从一个序列中，取出一个子序列（新序列）
* `序列` [ `起始下标` : `结束下标` : `步长`]

















































