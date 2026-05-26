# 开个好头说是

>闲话少说，就是做个学习记录吧，希望这个不会夭折。
>简单些，不要求很精美，每天记录一点点就行



## 1.英语翻译作业🥇

satellite navigation,

cover,
assist,  rescue, 
international standard book number
ISBN 
国际标准书号说是

>话说，快要四级了啊，得去学学英语了，u校园还没怎么做过hhh


## 2.编程相关

<details>
<summary>vector初始化方式</summary>

  | 初始化方式             | 示例代码                                            | 含义 / 说明                 |
| ----------------- | ----------------------------------------------- | ----------------------- |
| 空 vector          | `vector<int> v;`                                | 创建一个空的 `vector`         |
| 指定大小              | `vector<int> v(5);`                             | 创建 5 个元素，默认值为 `0`（基本类型） |
| 指定大小和初值           | `vector<int> v(5, 10);`                         | 创建 5 个元素，每个都是 `10`      |
| 列表初始化（推荐）         | `vector<int> v = {1,2,3};`                      | 直接初始化元素                 |
| 列表初始化（省略=）        | `vector<int> v{1,2,3};`                         | 与上面类似，C++11 风格          |
| 拷贝初始化             | `vector<int> v2(v1);`                           | 用另一个 `vector` 初始化       |
| 赋值初始化             | `vector<int> v2 = v1;`                          | 效果类似拷贝                  |
| 区间初始化             | `vector<int> v(arr, arr + n);`                  | 用数组区间初始化                |
| 用另一个 vector 的部分区间 | `vector<int> v(v1.begin(), v1.end());`          | 拷贝整个 `v1`               |
| 部分区间初始化           | `vector<int> v(v1.begin()+1, v1.begin()+4);`    | 拷贝 `[1,4)` 范围           |
| 二维 vector 初始化     | `vector<vector<int>> v(3, vector<int>(4));`     | 3 行 4 列，全是 `0`          |
| 二维 vector 指定初值    | `vector<vector<int>> v(3, vector<int>(4, -1));` | 3×4，全是 `-1`             |
| 动态扩容添加            | `cpp\nvector<int> v;\nv.push_back(1);\n`        | 先空着，后续添加元素              |
| 使用 assign         | `cpp\nvector<int> v;\nv.assign(5, 2);\n`        | 变成 5 个 `2`              |
| assign 区间         | `v.assign(v1.begin(), v1.end());`               | 用区间重新赋值                 |

</details>


>主要可以记住默认初始化为0， 两个参数的话右边的一般为初始值(也不一定，还有区间初始化

```c++
int my_round(double x)
{
    if(x >= 0)
        return (int)(x + 0.5);
    else
        return (int)(x - 0.5);
}
```
对正负数的四舍五入,

向下取整，负数则不符合，使用cmath中的库函数round

对于正整数：
`(a + b / 2) / b`

光棍数，感觉有点难，让我烧烤一下


算法题目，审题，考虑边界情况
>心思还是不够缜密，鉴定为练少了h
