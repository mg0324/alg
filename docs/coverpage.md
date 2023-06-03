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
              title: "位运算",
              remark: "左移、右移"
            },
            {
              title: "数据结构",
              remark: "数组、链表、堆、栈、队列、图、二叉树、并查集、单调栈、哈希表"
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
              remark: "阶乘、反转字符串、8皇后问题、汉诺塔"
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