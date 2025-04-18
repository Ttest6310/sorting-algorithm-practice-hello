[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=19036665&assignment_repo_type=AssignmentRepo)
# 排序算法实现作业

本作业要求你实现三种基本排序算法：冒泡排序、选择排序和插入排序。

## 任务要求

1. 在 `sorting.py` 文件中完成以下函数的实现：
   - `bubble_sort(arr)`：冒泡排序
   - `selection_sort(arr)`：选择排序
   - `insertion_sort(arr)`：插入排序

2. 所有函数应接受一个列表作为输入，并返回排序后的新列表，不应修改原始列表。

3. 你的实现将通过自动化测试进行评分。

## 算法说明

### 冒泡排序
- 冒泡排序通过重复遍历要排序的列表，比较相邻项并交换顺序错误的项
- 重复遍历直到没有交换发生，表示列表已排序完成

### 选择排序
- 选择排序通过从未排序部分找出最小元素，将其放到已排序部分的末尾
- 重复此过程直到所有元素都被排序

### 插入排序
- 插入排序通过构建已排序部分，并将未排序的元素一个个插入到已排序部分的正确位置
- 类似于玩扑克牌时整理手中的牌

## 示例

### 输入/输出示例

```python
# 示例1
输入: [3, 1, 4, 2]
输出: [1, 2, 3, 4]

# 示例2
输入: []
输出: []

# 示例3
输入: [5]
输出: [5]
```

### 冒泡排序示例实现

```python
def bubble_sort_example(arr):
    # 创建输入数组的副本，以免修改原始数组
    result = arr.copy()
    n = len(result)
    
    # 外循环：需要进行n-1次冒泡
    for i in range(n):
        # 内循环：比较相邻元素并交换
        for j in range(0, n-i-1):
            if result[j] > result[j+1]:
                # 交换元素
                result[j], result[j+1] = result[j+1], result[j]
    
    return result
```

## 评分标准

- 冒泡排序实现：30分
- 选择排序实现：30分
- 插入排序实现：30分
- 总分：90分

## 提交要求

1. 完成 `sorting.py` 文件中的函数实现
2. 确保所有测试用例通过
3. 不要修改测试文件或配置文件 