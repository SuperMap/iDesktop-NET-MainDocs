---
id: OtherMapExplain
title: 其他地图的制图要点说明
---
**中国行政区划横版地图**

  * 中国行政区地图标明由省至县的行政区划范围与行政中心，方便用作底图；
  * 南海诸岛附图的四至范围需要严格把握，不能随意绘制，并且附图中的要素在任何比例尺下都需要与主图要素保持一致；
  * 在行政区划图中，地区、自治州、盟不需要加点位符号，直接表示注记即可，并且这些地方的行政中心注记需要加下划线。

**经济区地图**

  * 制作用于打印出图的地图可以固定比例尺，只在当前比例尺下审视地图效果；
  * 普通的区域地图对行政点的注记位置要求比较严格，同一省（市）内的行政点注记必须在该省（市）内，使用移动标签的功能来适当调整标签的位置；
  * 使用同一色系的不同颜色来制造地图的层次感；
  * 区划要素的表达使用CAD数据集完成。

**热度图**

  * 由冷色到暖色或同一色系由浅至深的色彩渐变可以用来展现点要素相对密度或加权密度的变化；
  * 为热度图选择合适的颜色方案并分别为两个关键色设置透明度，使得突出专题要素热度分布的同时保留底图要素可读性；
  * 设置“权重字段”来控制离散点对于密度的影响程度；设置“核半径”来修改每个离散点的影响范围；设置“颜色渐变模糊度”与“最大颜色权重”以调整色带的渲染效果；
  * 在比例尺较小时如果要素过于聚集，使得点的密度分布规律被弱化，可以使用自定义最值，改善热度图显示效果。

**格网聚合图**

  * 网格颜色的变化可以直观展现聚合点和单一点代表的点数量差异，随着距离相近的格子聚合为一个格子显示，网格的颜色变暖或变深以反映所代表的点数变大；
  * 设置“格网字段”来控制离散点对于格网所代表数值的影响程度；
  * 为网格聚合图选择合适的颜色方案并为两个关键色设置透明度，使得突出专题要素分布状态的同时保留底图要素可读性，支持为关键色设置不同的透明度，此时系统会对颜色方案中的颜色进行透明度渐变；
  * 修改网格的边框线与标签风格可以改善地图显示效果，使用同色系不同明暗度的颜色可以在协调整体配色的同时丰富地图表现层次。

