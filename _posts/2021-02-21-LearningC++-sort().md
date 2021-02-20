
### 简介
1、sort函数可以三个参数也可以两个参数，必须的头文件#include < algorithm>和using namespace std;
2、它使用的排序方法是类似于快排的方法，时间复杂度为n*log2(n)
3、Sort函数有三个参数：（第三个参数可不写）

* 第一个是要排序的数组的起始地址。

* 第二个是结束的地址（最后一位要排序的地址）

* 第三个参数是排序的方法，可以是从大到小也可是从小到大，还可以不写第三个参数，此时默认的排序方法是从小到大排序。


### 示例
C++ 98 的写法是要先写一个compare函数：

```
bool compare(int &a, int &b)
{
    return a > b;  //降序排序
}
sort(a, a + n, compare);
```
然而，用ISO C++ 11 标准新增的Lambda表达式，可以这么写：

```
sort(a, a + n, [](int a, int b){return a > b;});   //降序排序
```

### <center> 表 1 C++ STL 用法</center>

|排序函数函数名|用法|
|--|--|
|sort (first, last)	|对容器或普通数组中 [first, last) 范围内的元素进行排序，默认进行升序排序。|
|stable_sort (first, last)	|和 sort() 函数功能相似，不同之处在于，对于 [first, last) 范围内值相同的元素，该函数不会改变它们的相对位置。|
|is_sorted (first, last)	|检测 [first, last) 范围内是否已经排好序，默认检测是否按升序排序。|
|is_sorted_until (first, last)	|和 is_sorted() 函数功能类似，唯一的区别在于，如果 [first, last) 范围的元素没有排好序，则该函数会返回一个指向首个不遵循排序规则的元素的迭代器。
|
