## Big-O Complexity Chart
| Big O explaination | Name        | Example                        |
| ------------------ | ----------- | ------------------------------ |
| O(1)               | Constant    | 通过数组下标找到元素           |
| O(log n)           | Logarithmic | 有序数组里用二分查找           |
| O(n)               | Linear      | 无序数组里查找一个元素         |
| O(n log n)         | Log-linear  | 归并排序、堆排序               |
| O(n^2)             | Quadratic   | 选择排序、插入排序、冒泡排序   |
| O(n^3)             | Cubic       | 复杂度太高啦啦（不知道例子捏） |
| O(2^n)             | Exponential | 找一个列表所有子集             |
| O(n!)              | Factorial   | 找一个列表所有排列             |


### Time Complexity of Common Operation
#### Array
| Operation                  | Time Complexity |
| -------------------------- | --------------- |
| 在结尾添加或删除元素       | O(1)            |
| 访问或修改任意索引处的元素 | O(1)            |
| 求给定前缀和的子数组的和   | O(1)            |
| 从任意索引中添加或删除元素 | O(n)            |
| 检查元素是否存在           | O(n)            |
| 构建前缀和                 | O(n)            |

#### Linked List
| Operation | Time Complexity |
| --------- | --------------- |
| Access    | O(n)            |
| Search    | O(n)            |
| Insert    | O(1)            |
| Delete    | O(1)            |

#### Hash Table
| Operation | Time Complexity |
| --------- | --------------- |
| Access    | O(1)            |
| Search    | O(1)            |
| Insert    | O(1)            |
| Delete    | O(1)            |

#### Binary Search Tree
| Operation | Time Complexity |
| --------- | --------------- |
| Access    | O(log n)        |
| Search    | O(log n)        |
| Insert    | O(log n)        |
| Delete    | O(log n)        |

#### Heap
| Operation | Time Complexity |
| --------- | --------------- |
| Access    | O(1)            |
| Search    | O(n)            |
| Insert    | O(log n)        |
| Delete    | O(log n)        |

#### Graph
| Operation | Time Complexity |
| --------- | --------------- |
| Access    | O(V + E)        |
| Search    | O(V + E)        |
| Insert    | O(1)            |
| Delete    | O(V + E)        |

### Space Complexity of Common Data Structures
| Data Structure     | Space Complexity |
| ------------------ | ---------------- |
| Array              | O(n)             |
| Linked List        | O(n)             |
| Hash Table         | O(n)             |
| Binary Search Tree | O(n)             |
| Heap               | O(n)             |
| Graph              | O(V + E)         |

### Space Complexity of Common Algorithm
| Algorithm           | Space Complexity |
| ------------------- | ---------------- |
| Recursion           | O(n)             |
| Dynamic Programming | O(n)             |
| Divide and Conquer  | O(n)             |
| Greedy              | O(1)             |
| Backtracking        | O(n)             |
