---
title: UCount - Online Mobile App for Accounting
cover: /image/UCount1.png
---
 **UCount** —  字学镜像计划1.0前端之在线记账系统实践项目  **[github](https://github.com/wuuusicong/UCount)**

- [x] 已通过项目考核    

- [x] 记账页面
- [x] 图表页面
- [x] 账单页面

---

##     技术栈

[Create React App](https://create-react-app.dev/) + [Ant Design Mobile](https://mobile.ant.design/zh) + [D3.js](https://d3js.org/) + [React Hooks](https://reactjs.org/docs/hooks-intro.html)     

​    



<img src="/../images/UCount.gif" class="UCountGif"/>

## 项目简介

实现一个在线记账的网站，用户可以在网站上管理每天的收入和支持，并以折线图的形式展示出不同维度的收支变化趋势。

包含Web端和Server端，使用轻服务进行网页托管、接口部署和数据存储。



### 用户需求

记账系统需要满足用户记录收入/支出、浏览账单、分析账单的能力。

#### 记账页面

- 用户可以在网页上记录自己单笔的收入/支出
- 一笔收入/支出可能包括记账时间、金额、花销类别、备注等
- 用户可以自由决定一笔记录的记账日期
- 用户可以更改自己的某一笔记录，例如金额、花销类别、备注，以及记账日期

#### 账单列表

- 用户可以浏览自己历史所有的记账记录，包括收入和支出
- 在账单列表页，用户可以清晰的看到自己的账单所在时间、类别和金额
- 用户可以看到自己当前所在月份的总收入和支出

#### 账单图表分析

用户可以分析自己的收入/支出情况。图表可以分为时间和花销类别两个大的维度。

#### •  时间维度：收入/支出趋势图

用户可以看到自己的收入/支出趋势图，图表可以是一周、一月或者一年的收入/支出趋势

#### •  花销类别维度：收入/支出占比

可以通过饼图或者其他方式，体现出用户的各类支出占比情况。

## 设计思路

### 组件架构分析

​      



![](/../images/UCount.svg)  

​    



### 数据流分析

​     



![](/../images/UCountData.svg)

## 遇到的问题

### 组件的UI和状态未剥离

使用了较多的局部context去控制整个页面的数据流。

![image-20220303211441168](/../images/u2.png)

这里使用了Date和Data两个context，用于控制筛选数据。

又比如在组件内部处理状态的变化(dateChange)等等，代码太冗余

![image-20220303211716625](/../images/image-20220303211716625.png)

### 局部状态的维护

![image-20220302215935883](/../images/image-20220302215935883.png)

#### **以前的解决方案**

引入全局的页面更新变量

![image-20220302220146704](/../images/image-20220302220146704.png)

![image-20220302220205479](/../images/image-20220302220205479.png)

对UI进行交互后，触发useEffect()去请求数据，并刷新页面。



### 表单的处理

### 
