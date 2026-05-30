
```c++
class NumArray {
public:
    vector<int> arr;
    NumArray(vector<int>& nums) {
        arr.resize(nums.size() + 1);
        
        for(int i = 0; i < nums.size(); i ++)
        {
            arr[i + 1] = arr[i] + nums[i];
        }
    }
    
    int sumRange(int left, int right) {
        return arr[right+1] - arr[left];
    }
};
```
<details>

  | 思想      | 在 `NumArray` 里的体现             | 本质目的             |
| ------- | ----------------------------- | ---------------- |
| 面向对象    | `class NumArray`              | 把“数据+功能”组织到一起    |
| 数据封装    | `vector<int> arr;`            | 数据藏在类内部，外部不用关心实现 |
| 构造函数初始化 | `NumArray(vector<int>& nums)` | 创建对象时完成初始化       |
| 预处理     | 构建前缀和 `arr[i+1]`              | 初始化时多做事，后面更快     |
| 空间换时间   | 多存一个前缀和数组                     | 用额外内存换 O(1) 查询   |
| 前缀和思想   | `arr[r+1] - arr[l]`           | 利用累计信息快速求区间和     |
| 接口设计    | `sumRange(left,right)`        | 只暴露功能，不暴露实现      |
| 抽象      | 用户只会调用 `sumRange()`           | 不需要知道内部怎么实现      |
| 数据结构设计  | 自己决定成员变量                      | 根据操作需求维护数据       |
| 查询优化    | 多次 `sumRange()`               | 把重复计算提前完成        |
| 状态维护    | `arr` 一直存在于对象内                | 对象长期保存信息         |
| 模块化     | 类负责自己的逻辑                      | 功能独立、易复用         |
| 算法复杂度优化 | 查询 O(n) → O(1)                | 提升效率             |
| 工程化思维   | “初始化 + 多次调用”                  | 更接近真实软件开发        |

</details>

