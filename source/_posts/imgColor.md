---
title: Image-guided color mapping for categorical data visualization
cover: /image/color.png
---
Image-guided color mapping for categorical data visualization （CVM 2021)

针对在类别数据可视化中存在的配色问题，提出了用图表来引导这类可视化的配色，可以帮助用户快速对类别可视化进行配色，能从样例图片上得到一个类区分度最大并且最美观的配色方案。

![image-20220304221509475](../images/image-20220304221509475.png)



## 核心思想

![image-20220304221622218](../images/image-20220304221622218.png)

**将图片映射到RGB三维空间中**，采用启发式的探索方法从图片中搜寻到相同类的数量的视觉差最大的颜色盘。

![image-20220304221918306](../images/image-20220304221918306.png)

根据提取出来的颜色盘，在结合可视化中类的分布(散点图)，进行颜色赋值。

## **效果展示**

### 饼图和柱状图

![image-20220304222025452](../images/c1.png)

###

### 散点图

![image-20220304222044508](../images/image-20220304222044508.png)

### 信息图的配色

![image-20220304222114222](../images/image-20220304222114222.png)
