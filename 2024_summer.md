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
n=arr.length
| Operation                  | Time Complexity                      |
| -------------------------- | ------------------------------------ |
| 在结尾添加或删除元素       | O(1)                                 |
| 访问或修改任意索引处的元素 | O(1)                                 |
| 求给定前缀和的子数组的和   | O(1)                                 |
| 从任意索引中添加或删除元素 | O(n)                                 |
| 检查元素是否存在           | O(n)                                 |
| 构建前缀和                 | O(n)                                 |
| 双指针                     | O(n·k),k为每次迭代的工作，如滑动窗口 |

#### String
n=s.length
| Operation                                | Time Complexity |
| ---------------------------------------- | --------------- |
| 任意索引处的访问元素                     | O(1)            |
| 添加或删除字符                           | O(n)            |
| 通过连接数组、stringbuilder 等构建字符串 | O(n)            |
| 创建子字符串                             | O(m)            |
| 两个字符串之间的连接                     | O(n+m)          |
| 双指针                                   | O(n·k)          |

#### Linked List
n=链表中节点数
| Operation                                  | Time Complexity |
| ------------------------------------------ | --------------- |
| 给定指针位置的后面添加或删除元素           | O(1)            |
| 如果是双向链表，给定指针位置添加或删除元素 | O(1)            |
| 在没有指针的任意位置添加或删除元素         | O(n)            |
| 无指针任意位置的访问元素                   | O(n)            |
| 检查元素是否存在                           | O(n)            |
| 使用快慢指针或哈希映射完成一次遍历         | O(1)            |
| 在位置 i 和 j 之间反转                     | O(j-i)          |

#### Hash Table
n=dic.length
| Operation                 | Time Complexity |
| ------------------------- | --------------- |
| 添加或删除键值对          | O(1)            |
| 检查 key 是否存在         | O(1)            |
| 访问或修改与 key 相关的值 | O(1)            |
| 检查值是否存在            | O(n)            |
| 遍历所有键值              | O(n)            |

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


以下是一个符合要求的 Markdown 文档：

# Big - O Complexity Chart
| Big O Explanation | Name         | Example                                                                            |
| ----------------- | ------------ | ---------------------------------------------------------------------------------- |
| O(1)              | Constant     | Finding an element by array subscript                                              |
| O(log n)          | Logarithmic  | Binary search in a sorted array                                                    |
| O(n)              | Linear       | Searching for an element in an unsorted array                                      |
| O(n log n)        | Log - linear | Merge sort, Heap sort                                                              |
| O(n²)             | Quadratic    | Selection sort, Insertion sort, Bubble sort                                        |
| O(n³)             | Cubic        | (High complexity, e.g., nested loops with three levels in some complex algorithms) |
| O(2ⁿ)             | Exponential  | Finding all subsets of a list                                                      |
| O(n!)             | Factorial    | Finding all permutations of a list                                                 |

## Time Complexity of Common Operation
### Array
Let $n = arr.length$
| Operation                                                  | Time Complexity                                                                                     |
| ---------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| Adding or deleting an element at the end                   | O(1)                                                                                                |
| Accessing or modifying an element at any index             | O(1)                                                                                                |
| Calculating the sum of sub - arrays for a given prefix sum | O(1)                                                                                                |
| Adding or deleting an element from any index               | O(n)                                                                                                |
| Checking if an element exists                              | O(n)                                                                                                |
| Building the prefix sum                                    | O(n)                                                                                                |
| Two - pointer approach                                     | $O(n \cdot k)$, where $k$ is the work done at each iteration (e.g., in a sliding - window scenario) |

### String
Let $n = s.length$
| Operation                                                      | Time Complexity                                 |
| -------------------------------------------------------------- | ----------------------------------------------- |
| Accessing an element at any index                              | O(1)                                            |
| Adding or deleting a character                                 | O(n)                                            |
| Building a string by concatenating arrays, StringBuilder, etc. | O(n)                                            |
| Creating a substring                                           | O(m) (where $m$ is the length of the substring) |
| Concatenating two strings                                      | O(n + m)                                        |
| Two - pointer approach                                         | $O(n \cdot k)$                                  |

### Linked List
Let $n$ be the number of nodes in the linked list
| Operation                                                                                  | Time Complexity |
| ------------------------------------------------------------------------------------------ | --------------- |
| Adding or deleting an element after a given pointer position                               | O(1)            |
| If it is a doubly - linked list, adding or deleting an element at a given pointer position | O(1)            |
| Adding or deleting an element at any position without a pointer                            | O(n)            |
| Accessing an element at any position without a pointer                                     | O(n)            |
| Checking if an element exists                                                              | O(n)            |
| Completing one traversal using fast - slow pointers or hash mapping                        | O(n)            |
| Reversing between positions $i$ and $j$                                                    | O(j - i)        |

### Hash Table
Let $n = dic.length$
| Operation                                         | Time Complexity |
| ------------------------------------------------- | --------------- |
| Adding or deleting a key - value pair             | O(1)            |
| Checking if a key exists                          | O(1)            |
| Accessing or modifying the value related to a key | O(1)            |
| Checking if a value exists                        | O(n)            |
| Traversing all key - value pairs                  | O(n)            |

### Binary Search Tree
| Operation | Time Complexity |
| --------- | --------------- |
| Access    | O(log n)        |
| Search    | O(log n)        |
| Insert    | O(log n)        |
| Delete    | O(log n)        |

### Heap
| Operation | Time Complexity |
| --------- | --------------- |
| Access    | O(1)            |
| Search    | O(n)            |
| Insert    | O(log n)        |
| Delete    | O(log n)        |

### Graph
| Operation | Time Complexity |
| --------- | --------------- |
| Access    | O(V + E)        |
| Search    | O(V + E)        |
| Insert    | O(1)            |
| Delete    | O(V + E)        |

## Space Complexity of Common Data Structures
| Data Structure     | Space Complexity |
| ------------------ | ---------------- |
| Array              | O(n)             |
| Linked List        | O(n)             |
| Hash Table         | O(n)             |
| Binary Search Tree | O(n)             |
| Heap               | O(n)             |
| Graph              | O(V + E)         |

## Space Complexity of Common Algorithm
| Algorithm           | Space Complexity |
| ------------------- | ---------------- |
| Recursion           | O(n)             |
| Dynamic Programming | O(n)             |
| Divide and Conquer  | O(n)             |
| Greedy              | O(1)             |
| Backtracking        | O(n)             |