---
id: Properties_Tab
title: 选项卡
---
**表格：选项卡属性**

属性 | 说明  
---|---  
ID | 选项卡支持多个不同配置文件里的项进行合并显示，合并的依据就是通过 id 来实现的，也就是说我们可以在 A 插件的配置文件中配置一个选项卡，指定一个 id，同时在 B 插件里面也配置一个选项卡，指定相同的 id，在系统显示时，这两个选项卡中的项将会合并到一起，放到一个选项卡上显示。  
标签 | 选项卡的显示名称，“开始”即为该选项卡的显示名称。  
插件 | 包含该界面元素的插件名称，即包含该界面元素定制内容的插件配置文件对应的名称。  
可见 | 指定该选项卡是否可见，该属性值为 true 时，表示可见，false 为不可见。  
所属窗体 | 指定该选项卡所绑定的窗体，主要目的是为了实现特定类型的窗口需要有特定的功能，默认情况下与主窗口绑定。例如，地图操作相关的功能只有在地图窗口中才有效，因此，可以控制只有当存在地图窗口时，该部分功能才可以显示。这样就可以将地图操作相关功能放置在一个选项卡中，然后将该选项卡与地图窗口绑定，在应用过程中，只有存在地图窗口时，该选项卡才会显示在功能区中，否则不出现。  
索引 | 用于排序功能区上的选项卡（tab 页），即当功能区存在多个选项卡时，每个选项卡将通过该项的值来确定其在功能区的排列次序。  
