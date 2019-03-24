---
title: Hexo流程图
date: 2019-03-24 14:43:25
tags: Hexo
---


## Install

```bash
npm install --save hexo-filter-flowchart
```

## Usage

This plugin is based on  [flowchart.js](https://github.com/adrai/flowchart.js), so you can defined the chart as follow:

{% codeblock 示例 https://github.com/bubkoo/hexo-filter-flowchart hexo-filter-flowchart %}
st=>start: Start|past:>http://www.google.com[blank]
e=>end: End:>http://www.google.com
op1=>operation: My Operation|past
op2=>operation: Stuff|current
sub1=>subroutine: My Subroutine|invalid
cond=>condition: Yes
or No?|approved:>http://www.google.com
c2=>condition: Good idea|rejected
io=>inputoutput: catch something...|request

st->op1(right)->cond
cond(yes, right)->c2
cond(no)->sub1(left)->op1
c2(yes)->io->e
c2(no)->op2->e
{% endcodeblock %}

```flow
st=>start: Start|past:>http://www.google.com[blank]
e=>end: End:>http://www.google.com
op1=>operation: My Operation|past
op2=>operation: Stuff|current
sub1=>subroutine: My Subroutine|invalid
cond=>condition: Yes
or No?|approved:>http://www.google.com
c2=>condition: Good idea|rejected
io=>inputoutput: catch something...|request

st->op1(right)->cond
cond(yes, right)->c2
cond(no)->sub1(left)->op1
c2(yes)->io->e
c2(no)->op2->e
```

### 语法


| 操作模块 | 说明 |
|--|--|
| start | 开始 |
| end | 结束 |
| opration | 普通操作块 |
| condition | 判断块 |
| subroutine | 子任务块 |
| inputoutput | 输入输出块 |

## 参考
[flowchart.js](https://flowchart.js.org/)
[hexo-filter-flowchart](https://github.com/bubkoo/hexo-filter-flowchart)