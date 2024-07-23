## Template

### 1. Double points
case1
```cpp
int fn(vector<int>& arr){
    int left = 0;
    int right = int(arr.size()) -1;
    int ans = 0;

    while(left < right){
        if(CONDITION){
            //necessary code
            left++;
        }
        else{
            right++;
        }
    }
    return ans;
}
```

```python
def fn(arr):
    left = ans = 0
    right = len(arr) - 1

    while left < right:
        #necessary code
        left += 1
    else:
        right -= 1
    return ans
```
case 2

```cpp
int fn(vector<int>& arr1, vector<int>& arr2){
    int i = 0, j = 0, ans = 0;

    while(i < arr1.size() && j < arr2. size()){
        if(CODITION){
            i++;
        }else{
            j++;
        }
    }

    while(i < arr1.size()){
        i++;
    }
    
    while(j < arr2.size()){
        j++;
    }

    return ans;
}
```

```python
def fn(arr1, arr2):
    i = j = ans = 0

    while i < len(arr1) and j < len(arr2):
        i += 1
    else:
        j += 1

    while i < len(arr1):
        i += 1
    while j < len(arr2):
        j += 1
    return ans
```
### 2.Sliding windows
```cpp
int fn(vector<int>& arr){
    int left = 0, ans = 0, curr = 0;
    
    for(int right = 0; right < arr.size(); right++){
        //adding code to add "arr[right]" to "curr"
        while(WINDOW_CONDITION_BROKEN){
            //delete "arr[left]" from "curr"
            left++;
        }
        //update ans
    }
    return ans;
}
```

```python
def fn(arr):
    left = ans = curr = 0

    for right in range(len(arr)):
    //adding code to add "arr[right]" to "curr"
        while WINDOW_CONDITION_BROKEN:
            left += 1
            //update ans
    return ans
```

### 3. Build the prefix "and"
```cpp
vector<int> fn(vector<int>& arr){
    vector<int> prefix(arr.size());
    prefix[0] = arr[0];

    for(int i = 1; i < arr.size(); i++){
        prefix[i] = prefix[i - 1] + arr[i];
    }

    return prefix;
}
```

```python
def fn(arr):
    prefix = [arr[0]]
    for i in range(1, len(arr)):
        prefix.append(prefix[-1] + arr[i])

    return prefix
```

### 4. High efficiency string construct
```cpp
string fn(vector<char>& arr){
    return string(arr.begin(), arr.end())
}
```

```python
def fn(arr):
    ans = []
    for c in arr:
        ans.append(c)
    return "".join(ans)
```

### 5. Link: fast and slow points
```cpp
int fn(ListNode* head){
    ListNode* slow = head;
    ListNode* fast = head;
    int ans = 0;

    while(fast != nullptr && fast->next != nullptr){
        //necessary code
        slow = slow->nest;
        fast = fast->nest->next;
    }

    return ans;
}
```

```python
def fn(head):
    slow = head
    fast = head
    ans = 0

    while fast and fast.next:
        #necessary code
        slow = slow.next
        fast = fast.next.next

    return ans

```

### 6. Reverse link
```cpp
ListNode* fn(ListNode* head){
    ListNode* curr = head;
    ListNode* prev = nullptr;
    while (curr != nullptr){
        ListNode* nextNode = curr->next;
        curr->next = prev;
        prev = curr;
        curr = nextNode;
    }

    return prev;
}
```

```python
def fn(head):
    curr = head
    prev = None
    while curr:
        nextNode = curr.next
        curr.next = prev
        prev = curr
        curr = nextNode
    return prev
```

### 7.find the exact array number
```cpp
int fn(std::vector<int>& arr, int k){
    std::unordered_map<int, int> counts;
    counts[0] = 1;
    int ans = 0, curr = 0;

    for(int num: arr){
        // change curr based on the problem
        ans += counts[curr - k];
        counts[curr]++;
    }
    
    return ans;
}
```

```python
from collections import defaultdict

def fn(arr, k):
    counts = defaultdict(int)
    counts[0] = 1
    ans = curr = 0

    from num in arr:
        # change curr based on the problem

```
###  8. monotonically incremental
```cpp
int fn(std::vector<int>& arr) {
    std::stack<int> stack;
    int ans = 0;

    for (int num: arr) {
        // decrease change the compare sign
        while (!stack.empty() && stack.top() > num) {
            // 根据题意补充代码
            stack.pop();
        }

        stack.push(num);
    }
}

```

```python
def fn(arr):
    stack = []
    ans = 0

    for num in arr:
        # change > to < when necessary
        while stack and stack[-1] > num:
            # complete the code
            stack.pop()
        stack.append(num)
    
    return ans
```

### 9.Binary tree / Deep First Search (recursive)
```cpp
int dfs(TreeNode* root){
    if(root == nullptr){
        return 0;
    }
    int ans = 0;
    //complete the code
    dfs(root.left);
    dfs(root.right);
    return ans;
}
```

```python
def dfs(root):
    if not root:
        return
    ans = 0
    #complete code
    dfs(root.left)
    dfs(root.right)
    return ans
```

### 10.Binary tree / Deep First Search (iteration)
```cpp
int dfs(TreeNode* root){
    stack<TreeNode*> stack;
    stack.push(root);
    int ans = 0;

    while(!stack.empty()){
        TreeNode* node = stack.top();
        stack.pop();
        //complete the code
        if(node->left != nullptr){
            stack.push(node->left);
        }
        if(node->right != nullptr){
            stack.push(node->right);
        }
    } 
    return ans;
}
```
### 11.Binary tree / Breath First Search
```cpp
int fn(TreeNode* root){
    queue<TreeNode*> queue;
    queue.push(root);
    int ans = 0;

    while(!queue.empty()){
        int currentLength = queue.size();

        for (int i = 0; i < currentLength; i++){
            TreeNode* node = queue.front();
            queue.pop();
            //based on the question to complete the code
            if(node->left != nullptr){
                queue.push(node->left);
            }
            if(node->right != nullptr){
                queue.push(node->right);
            }
        }
    }
    return ans;
}
```

```python
from collections import deque

def fn(root):
    queue = deque([root])
    ans = 0

    while queue:
        currentLength = len(queue)
        #do current operation
        for _ in range(currentLength):
            node = queue.popleft()
            if node.left:
                queue.append(node.left)
            if node.right:
                queue.append(node.right)
    return ans

```
### 12.Graph / Depth First Search (recursive)
assume the node number range from 0 to n-1
the graph is given with the format of graph
```cpp
unordered_set<int> seen;
int fn(vector<vector<int>>& graph){
    seen.insert(START_NODE);
    return dfs(START_NODE, graph);
}

int fn dfs(int node, vector<vector<int>>& graph){
    int ans = 0;
    for(int neighbor: graph[node]){
        if(seen.find(neighbor) == seen.end()){
            seen.insert(neighbor);
            ans += dfs(neighbor, graph);
        }
    }
    return ans;
}
```
```python
def fn(graph):
    def dfs(node):
        ans = 0
        # complete based on the problem
        for neighbor in graph[node]:
            if neighbor not in seen:
                seen.add(neighbor)
                ans += dfs(neighbor)
        return ans
    seen = {START_NODE}
    return dfs(START_NODE)
```

### 13.Graph / Depth First Search (iteration)
```cpp
int fn(vector<vector<int>>& graph){
    stack<int> stack;
    unordered_set<int> seen;
    stack.push(START_NODE);
    seen.insert(START_NODE);
    int ans = 0;

    while(！stack.empty()){
        int node = stack.top();
        stack.pop();
        for(int neighbor: graph[node]){
            if(seen.find(neighbor) == seen.end()){
                seen.insert(neighbor);
                stack.push(neighbor);
            }
        }
    }
}
```

```python
def fn(graph):
    stack = [START_NODE]
    seen = [START_NODE]
    ans = 0

    while stack:
        node = stack.pop();
        #complete the code based on problem
        for neighbor in graph[node]:
            if neighbor not in seen:
                seen.add(neighbor)
                stack.append(neighbor)
    return ans
```
### 14.Graph / Bidth First Search
```cpp
int fn(vector<vector<int>>& graph){
    queue<int> queue;
    unordered_set<int> seen;
    queue.add(START_NODE);
    seen.insert(START_NODE);
    int ans = 0;

    while(!queue.empty()){
        int node = queue.front();
        queue.pop();//clean the queue
        //complete the code based on the problem
        for (int neighbor: graph[node]){
            if(seen.find(neighbor) == seen.end()){
                seen.insert(neighbor);
                queue.push(neighbor);
            }
        }
    }
}

```

```python
from collections import deque

def fn(graph):
    queue = deque([START_NODE])
    seen = [SATRT_NODE]
    ans = 0

    while queue:
        node = queue.popleft()
        #complete the code based on the problem
        for neighbor in graph[node]:
            seen.add(neighbor)
            queue.append(neighbor)
    return ans

```

### 15.find the first k element in the heap
```cpp
vector<int> fn(vector<int>& arr, int k){
    priority_queue<int, CRITERIA> heap;
    for(int num: arr){
        heap.push(num);
        if(heap.size()>k){
            heap.pop();
        }
    }

    vector<int> ans;
    while(heap.size()>0){
        ans.push_back(heap.top());
        heap.pop();
    }
    return ans;
}
```

```python
import heapq

def fn(arr, k):
    heap = []
    for num in arr:
        #add code based on the condition
        heapq.heappush(heap,(CRITERIA,num))
        if len(heap) > k:
            heapq.heappop(heap)
    return [num for num in heap]
```

