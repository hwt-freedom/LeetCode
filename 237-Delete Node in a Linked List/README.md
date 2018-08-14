## LeetCode 237.Delete Node in a Linked List

#### 问题分析：    
* 通常删除节点是通过将头指针遍历到需要删除的节点位置，并且删除节点时需要知道前一节点，因此本题的解题思路是将下一个节点的值拷贝给当前要删除的节点，再删除下一个节点，最终能够实现节点的删除操作。
#### 操作理解：
* 在节点拷贝时，不仅仅拷贝数据域，拷贝的还有指针域

### 参考大神的代码后
#### C++知识点：
* [【C++11】新特性——auto的使用](https://blog.csdn.net/huang_xw/article/details/8760403)