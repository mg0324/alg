<style type="text/css">
.coverpage{
  width:80%;
  margin:0 auto;
}
.coverpage .logo-text{
  border-radius: 10px;
  line-height: 80px;
  padding: 20px;
  font-size: 16px;
  background: #67C23A;
  color: #fff;
}
.coverpage .future-remark{
  color:gray;
  font-size:14px;
  min-height:60px;
}
.coverpage .future-card{
  margin:8px;
}
.coverpage .footer{
  text-align:center;
  color:gray;
  padding-top:10px;
}
.coverpage .footer a{
  font-size:14px;
}
.coverpage .desc{
  padding-bottom: 20px;
  text-align: left;
  line-height: 25px;
}

@media only screen and (max-width: 500px) {
  .coverpage{
    width:98%;
    margin:0 auto;
  }
  .coverpage .logo-text{
    border-radius: 10px;
    line-height: 80px;
    padding: 20px;
    font-size: 16px;
    background: #67C23A;
    color: #fff;
  }
  .desc{
    width:100%;
  }
}
</style>

<div class="coverpage">
  <el-result style="margin:0 auto;">
    <template slot="icon">
      <div class="logo-text">{{title}}</div>
    </template>
    <template slot="extra">
      <div class="desc" v-html="desc"></div>
      <el-button type="default" size="medium" @click="handleClick('README')">查看主页</el-button>
      <el-button type="primary" size="medium" @click="handleClick('ds/index')">数据结构</el-button>
    </template>
  </el-result>
  <el-row>
    <el-col :xs="24" :md="8" v-for="(item,index) in futures">
      <el-card shadow="hover" class="future-card">
        <h3>{{item.title}}</h3>
        <div v-html="item.remark" class="future-remark">
        </div>
      </el-card>
    </el-col>
  </el-row>
  <div v-html="footer" class="footer">
  </div>
</div>

<script type="text/javascript">
(
  {
    data(){
      return {
          footer: window.$mangodoc.footer,
          title: '猫大刚学算法',
          desc: "学习数据结果和算法后整理的笔记",
          futures: [
            {
              title: "一些概念",
              remark: "常数操作、时间复杂度、空间复杂度、对数器、比较器"
            },
            {
              title: "位运算",
              remark: "最右位是1、异或交换、得到最右位为1的数字、计算中点值"
            },
            {
              title: "数据结构",
              remark: "数组、链表、堆、栈、队列、图、二叉树、并查集、单调栈、哈希表"
            },
            {
              title: "字符串和数组",
              remark: "字符串子串搜索之KMP算法"
            },
            {
              title: "链表",
              remark: "单链表、双链表、环形链表、快慢指针"
            },
            {
              title: "栈",
              remark: "先进先出、有效的括号、可做DFS实现"
            },
            {
              title: "队列",
              remark: "后进先出、优先级队列、双端队列、可做BFS实现"
            },
            {
              title: "二叉树",
              remark: "二叉树遍历（BFS、DFS）、平衡二叉树、二叉搜索树、满二叉树、完全二叉树、序列化和反序列化、前缀树、红黑树"
            },
            {
              title: "堆",
              remark: "HeapInsert和Heapify、数组实现堆、优先级队列"
            },
            {
              title: "图",
              remark: "什么是图、存储方式、邻接表实现、图的创建、遍历、拓扑排序、最小生成树之Prim和Kruskal算法、最短路径之Dijkstra算法"
            },
            {
              title: "位图",
              remark: "Java实现位图、Linux系统权限设计、亿级URL黑名单判断设计、布隆过滤器"
            },
            {
              title: "并查集",
              remark: "Java实现并查集"
            },
            {
              title: "哈希表",
              remark: "哈希函数、哈希表实现、一致性哈希算法"
            },
            {
              title: "排序",
              remark: "冒泡、插入、选择、快速、归并、堆排序"
            },
            {
              title: "搜索",
              remark: "遍历、DFS、BFS、二分"
            },
            {
              title: "递归",
              remark: "master公式、阶乘、反转字符串、8皇后问题、汉诺塔"
            },
            {
              title: "索引",
              remark: "红黑树、B树、B+树"
            }
          ]
      }
    },
    methods: {
        handleClick(url) {
          window.location.href = "/#/"+url;
          window.location.reload();
        }
    }
  }
)
</script>