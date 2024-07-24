---
marp: true
size: 16:9
theme: am_blue
paginate: true
headingDivider: [2,3]
footer: \ *starAndHonor* *图论欢乐赛* *2024年6月24日*
---

<!-- _class: cover_a 
<!-- _header: "" --> 
<!-- _footer: "" --> 
<!-- _paginate: "" --> 
# 图论欢乐赛

starAndHonor
北师大台州附属高级中学
2024.7.18

## 目录

<!-- _class: col1_ol_sq fglass -->
- 狼烟起[T479387](https://www.luogu.com.cn/problem/T479387)
- Shortest Path on a Line[T479702](https://www.luogu.com.cn/problem/T479702)
- 「PHOI-1」路虽远[P9549](https://www.luogu.com.cn/problem/P9549)
- [BJWC2010] 严格次小生成树[P4180](https://www.luogu.com.cn/problem/P4180)


## 狼烟起[T479387](https://www.luogu.com.cn/problem/T479387)
原题LOJ    https://loj.ac/p/10094
送分。
Tarjan板子
统计一下入度为0的SCC个数即可
## Shortest Path on a Line[T479702](https://www.luogu.com.cn/problem/T479702)
原题atcoder    https://www.luogu.com.cn/problem/AT_nikkei2019_2_qual_d    
暴力建立边MLE+TLE
**正解**：操作理解为先从区间左边界 $l$ 点，再到达右边界 $r$ 点，再到达区间内一点，再到与其所连点。
所以，在 $l$ 与 $r$ 之间连一条长为 $c$ 的单向边由i向i-1建立边权为0的边单向边
## 「PHOI-1」路虽远[P9549](https://www.luogu.com.cn/problem/P9549)
Subtask0:暴力搜索
Subtask1:只有绿灯，直接最短路
Subtask2:没有黄灯，只需处理限速，限速k条等价于最多经过 m−k 条不限速的道路，建立m-k层图，图之间使用不限速边相连
Subtask3:考虑DP,dp[i][j][t]为当前点为 i ，闯了 j 次黄灯($j \le g$)，目前经过了 t 条没有限速的边($t \le m-k$)
如何判断当前是啥灯,dis%(x+y+z)
红绿灯考虑限速，黄灯还要考虑闯
答案是所有的$min_{j = 1}^{g}{min_{t = 1}^{k}}{dp[n][j][t]}$
## [BJWC2010] 严格次小生成树[P4180](https://www.luogu.com.cn/problem/P4180)
暴力教一下，正解自己去研究
暴力:枚举一条边，删除，求Kruskal，判断是否次小生成树
## 欢迎交流~~~ 

<!-- _class: trans -->
<!-- _footer: "" -->
<!-- _paginate: "" -->
<div>
<img src = "./images/R-C.png" style = "background-color: rgba(0, 0, 0, 0); margin-left: 400px;margin-bottom: px;" width = 300 >
</div>

