## 链表
链表有`单链表`、`双链表`和`环形链表`等。

* 单链表

![](https://mg.meiflower.top/oss/alg/ds/linktable/one.png)

* 双链表

![](https://mg.meiflower.top/oss/alg/ds/linktable/double.png)

* 环形链表

![](https://mg.meiflower.top/oss/alg/ds/linktable/loop.png)

### 优点  
1. 灵活分配内存空间。
2. 能在`O(1)`删除或添加元素。
### 缺点
1. 查询元素需要`O(n)`时间。

### 技巧
* 快慢指针（`slow`走一步，`fast`走2步）
* 虚假链表头
