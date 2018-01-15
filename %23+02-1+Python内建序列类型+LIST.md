
# 02-1 Python内建序列类型  LIST

## 1、LIST(清单或列表)


```python
# 建立一个list对像
a=[2,3,4,5,2,1,4,6,8,9]

#打印a中的所有元素
for i in a:
    print(i)

print('-'*30)

#打印a中的index及元素（range也是Python的列表类型）
for j in range(len(a)):
    print('第',j,'个元素：',a[j])

print('-'*30)
```

## 2、 可以对列表操作的运算
    x in s        true if an item of s is eaual to x,else False 
    x not in s     False if an item of s in eaual to x,else True
    s+t          the concatenation of s and t
    s*n 或 n*s     equivalent to adding s to itself n times
    s[i]         ith item of s,origin 0
    s[i:j]        slice of s from i to j
    s[i:j:k]      slice of s from i to j with step k
    len(s)       length  of s
    min(s) max(s）  smallest item of s  or  largest item of s
    s.index(x[,i[,j]]) index of the first occurrence of x in s
                 ( at or after index i and before index j)
    s.count(x)     total number of occurences of x in s


```python
#建立一个list对像
a=[2,4,5,6,2,1,4,6,8,9,2]
print(a)
print('-'*30)

#是否存在list中
print('10是否存在：',10 in a)
print('-'*30)

#范围
print('索引值3，4，5的元素：',a[3:6])
print('-'*30)

#长度
print('长度：',len(a))
print('-'*30)

#计算个数
print('2的个数',a.count(2))
print('-'*30)
```

    [2, 4, 5, 6, 2, 1, 4, 6, 8, 9, 2]
    ------------------------------
    10是否存在： False
    ------------------------------
    索引值3，4，5的元素： [6, 2, 1]
    ------------------------------
    长度： 11
    ------------------------------
    2的个数 3
    ------------------------------
    

## 3 可以在Mutable上操作的运算
    s[i]=x   item i of s is replaced by x
    s[i:j]=t  slice of s from i to j is replaced by the contents of the iterable t
    del s[i:j]   same as s[i:j]=[]
    s[i:j:k]=t   the elements of s[i:j:k] are replaced by those of t
    del s[i:j:k]  removes the elements of s[i:j:k] from the list
    s.append(x)  appends x to the end of the sequence(same as s[len(s):len(s)]=[x])
    s.clear()  removes all items from s(same as del s[:])
    s.copy()   creates a shallow copy of s(same as s[:])
    s.extend(t)  extends s with the contents of t(for the most part the same as s[len(s):len(s)]=t
    s+=t       same to uper
    s*=n     updates s with its contents repeated n times
    s.insert(i,x)   inserts x into s at the index given by i(same as s[i:i]=[x])
    s.pop([i])     retrieves the item at i and also removes it from s
    s.remove(x)    remove the first item from s where s[i]==x
    s.reverse()    reverses the items of s in place   



```python
#定义一个list对象
a=[2,4,5,6,2,1,4,6,8,9]

print(a)
print(type(a))
print('-'*40)

# 增加1个元素（在最后面）
a.append(10)
print(a)
print('-'*40)

#增加1个元素（在指定位置）
a.insert(1,100)
print(a)
print('-'*40)

#删除list中的第1个符合元素
a.remove(5)
print(a)
print('-'*40)

#替换指定的几个元素，要一一对应
a[3:8:2]=[10,20,30]
print(a)

#弹出一个指定的元素并删除
a.pop(4)
print(a)
```

    [2, 4, 5, 6, 2, 1, 4, 6, 8, 9]
    <class 'list'>
    ----------------------------------------
    [2, 4, 5, 6, 2, 1, 4, 6, 8, 9, 10]
    ----------------------------------------
    [2, 100, 4, 5, 6, 2, 1, 4, 6, 8, 9, 10]
    ----------------------------------------
    [2, 100, 4, 6, 2, 1, 4, 6, 8, 9, 10]
    ----------------------------------------
    [2, 100, 4, 10, 2, 20, 4, 30, 8, 9, 10]
    [2, 100, 4, 10, 20, 4, 30, 8, 9, 10]
    
