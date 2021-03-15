## 差分隐私（Differential Privacy）
阻止从输出推出输入
构建两个只相差一个记录的数据集

### 1、敏感度
- 对于两个相邻数据集D和D’相差一个记录，M的敏感度是M在所有可能的输入上的输出中的最大变化
- 实现方案：在现实数据集上搜索（构造）两名（或多名）浏览历史相似的用户行为数据，固定候选集，对所有的ranking结果进行显著性差异检验（使用Wilcox检验，双侧检验）

### 2、attack：能获取的真实数据越多，模型的隐私保护越差
- Membership inference attack / attribute inference attack
- 论文中使用的数据集和模型为图形分类任务，调研新闻推荐系统里是否有Membership inference attack的相关研究

### 3、KDD’09
- mask；添加噪音，然后看输出的变化

