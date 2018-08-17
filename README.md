代码性能优化总结
====================================================

#### 1、数组循环
```
1) 数组循环
2) 数组长度提取出来
3) 采用倒序
4) 循环嵌套外大内小
5) 循环嵌套提取不需要循环逻辑
6) 异常循环写循环外面
7) 

for in 比for loop慢非常多，至少20倍
FF对forEach比for loop好一点，但Chrome/IE性能差
FF/Chrome缓存Array.length比直接用要慢一点
map比foreach要快
map会返回一个新数组，数组中元素为原始数组元素调用函数处理后的值，不对原始数组产生影响；
map按照原始数组元素顺序依次处理元素，不会对空数组进行检测；
foreach不会产生新数组，foreach返回undefined
map因为返回数组 所以可以链式操作，foreach不能
map里面可以用return，
foreach里用return不起作用，foreach不能用break，会报错；

数组实例的find()和findIndex()
```