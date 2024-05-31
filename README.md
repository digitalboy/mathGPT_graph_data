# 说明

本数据集属于**数学根因分析与练习系统（Root Cause Analysis and Exercises for Mathematics, RCAE）**的基础子项目之一。旨在可以高效的发现学生数学学业错误的根本原因。

## 总项目介绍

**数学根因分析与练习系统（RCAE）**是一款利用先进的图数据库技术和强大的数据分析算法，旨在革新数学教育的系统。通过对学生答题记录的分析，RCAE能够快速定位学生掌握不牢固的知识点，并生成个性化的练习计划，帮助学生高效提升数学成绩。

## 此数据集的意义

本数据集是“数学根因分析与练习系统（RCAE）”的一个子项目，包含由中国背景师范大学出版社出版的小学数学全部知识点的详尽知识图谱。通过这个数据集，可以实现对小学数学知识点的全面了解和掌握，辅助RCAE系统进行更准确的根因分析和个性化练习推荐。

## 此数据集的优势
1. **充分MECE**：已经尽可能的将知识点做到不缺失，不遗漏，不重复，相互独立。
2. **关系充分**：从先决关系、包含关系、互补关系等12种关系。基本覆盖了数学领域的所有关系。

## 后续发展计划
1. **更多数据**：继续拓展初中，高中各个年级；人教出版社，北美数学……
2. **知识点解释**：为每个知识点提供生动、传神、有趣的解释，提高可理解性并降低学生的认知负荷。
3. **题目设计**：根据布鲁姆目标分类和孩子的认知规律，为每个知识点设计题目，难度分层。
4. **根因溯源**：可以快速的找到错题的根因，谨防无效刷题（我最恨这个了）。
5. **教师界面**：老师可以随时查看各种数据透视，快速掌握群体、个体的学业水平。
6. **结合脑科学**：学习尽快不能很快乐，但是尽量不要伤害孩子的学习热情。


## 使用方法

1. **下载数据集**：从GitHub仓库下载JSON格式的知识点图数据。
2. **加载数据**：将下载的JSON数据导入图数据库（如Neo4j）。
3. **构建知识图谱**：使用图数据库工具构建知识点之间的关系图谱。


## 目前存在的问题

尽管已经具备的相当的可用性，但是由于本人精力有限，才疏学浅。难免疏漏。

1. **数据完整性**：数据集可能存在某些知识点的缺失或描述不完整的情况，需要持续完善。
2. **关系准确性**：知识点之间的关系需要进一步验证和优化，确保其准确性和逻辑性。
3. **系统兼容性**：不同图数据库的兼容性和性能差异可能影响知识图谱的构建和查询效率。
4. **用户反馈**：需要更多的用户反馈来优化系统的算法和数据结构，提高整体效果。

## 需要的帮助
1. **编程**：如果您有编程能力，并热爱AI+教育，联系我。
2. **一线教师**：如果您能在一线实践并检测这个系统，联系我。
3. **脑科学**：如果您对教育+认知科学有兴趣，联系我。

## 联系作者

如有任何问题或建议，请通过以下方式联系作者：

- **微信**：13510546101
- **邮箱**：digitalboyzone@gmail.com
- **Twitter**：https://x.com/freethisslave

欢迎大家提供宝贵意见和建议，共同完善数学根因分析与练习系统！

## 关系(edge)表：
```
[
    {
        "type": "Prerequisite",
        "direction": "directed",
        "description": "描述一个概念是理解另一个概念的先决条件。",
        "example": {"from": "加法", "to": "乘法"}
    },
    {
        "type": "Includes",
        "direction": "directed",
        "description": "表明一个概念是另一个更广泛概念的一部分。",
        "example": {"from": "三角形", "to": "几何图形"}
    },
    {
        "type": "RelatedTo",
        "direction": "undirected",
        "description": "表示两个概念之间的相关性或关联性。",
        "example": {"from": "概率", "to": "统计"}
    },
    {
        "type": "AppliedIn",
        "direction": "directed",
        "description": "指一个概念如何在另一个领域或实例中被应用。",
        "example": {"from": "几何学", "to": "建筑设计"}
    },
    {
        "type": "AdvancesTo",
        "direction": "directed",
        "description": "表明一个概念是另一个概念的深入或拓展。",
        "example": {"from": "基础代数", "to": "高等代数"}
    },
    {
        "type": "ContrastsWith",
        "direction": "undirected",
        "description": "描述两个概念之间的对比或差异。",
        "example": {"from": "离散数学", "to": "连续数学"}
    },
    {
        "type": "SynonymousWith",
        "direction": "undirected",
        "description": "用于连接意思相近或相同的不同表述的概念。",
        "example": {"from": "减法", "to": "差运算"}
    },
    {
        "type": "HistoricallyDevelopedFrom",
        "direction": "directed",
        "description": "反映了概念的历史发展或演变。",
        "example": {"from": "古典代数", "to": "现代代数"}
    },
    {
        "type": "SubsetOf",
        "direction": "directed",
        "description": "表示一个概念是另一个概念的子集。",
        "example": {"from": "有理数", "to": "实数"}
    },
    {
        "type": "SpecialCaseOf",
        "direction": "directed",
        "description": "表示一个概念是另一个更一般概念的特殊情况。",
        "example": {"from": "正方形", "to": "矩形"}
    },
    {
        "type": "AnalogousTo",
        "direction": "undirected",
        "description": "表示两个概念在不同情境下具有类似的结构或性质。",
        "example": {"from": "平面几何", "to": "立体几何"}
    },
    {
        "type": "ComplementaryTo",
        "direction": "undirected",
        "description": "表示两个概念在一定程度上互为补充。",
        "example": {"from": "微分", "to": "积分"}
    }
]

```