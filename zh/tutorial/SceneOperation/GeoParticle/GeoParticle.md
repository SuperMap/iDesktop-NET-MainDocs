---
id: GeoParticle
title: 粒子效果的实现  
---  
**粒子系统简介**

粒子系统是三维计算机图形学中模拟一些特定的模糊显现的技术，而这些现象用其它传统的渲染技术难以表现出其真实感。经常使用粒子系统模拟的现象有火、爆炸、烟、水流、火花、落叶、云、雾、雪、尘、流星尾迹或者像发光轨迹这样的抽象视觉效果等。

**SuperMap 粒子系统结构介绍**

产品对传统的粒子系统结构进行了调整，每个三维粒子几何对象均由一个或若干粒子系统对象的共同作用来表现，三维粒子几何对象的结构如下图所示：     

![](img/GeoParticle.png)  

  
从上图可知，三维粒子几何对象中包含若干粒子系统对象，每个粒子系统对象均包含：一个或若干粒子发射器和一个粒子影响器，其中粒子发射器用于控制发射出来粒子的速度、方向等；粒子影响器则按照一定规则对粒子的路径和生命周期进行影响，使粒子效果更为真实。

### ![](../../img/read.gif)粒子特效实例

桌面应用程序中提供了" **粒子对象** "绘制功能。实现了三维场景中粒子特效展示的效果。

下边是 SuperMap 桌面系统中提供的几种粒子特效的实例，针对实例我们来简单了解下SuperMap 提供的粒子对象的结构、参数和效果展示。

###

![](img/close.gif)粒子特效参数对照

以下是粒子特效实例的部分参数值和效果对照 。

表中没有列出的参数粒子对象取默认值0，具体各项参数可参照[粒子对象创建](GeoParticleSetting)文档。

包括效果类型  粒子对象参数（单位：米） 、 粒子系统及影响其参数（单位：米） 、 发射器参数（单位：个/秒） 、 效果 等。

火焰 

**高度模式** ：绝对高度

**位置** ：（X，Y，Z)随机取值

**缩放** ：(X：1，Y：1，Z：1)

**粒子高度** ：5

**粒子宽度** ：6

**布告板模式** ：标准点布告板

**其他影响器作用** ：默认状态是关闭的

**发射频率** ：220个/秒

**初速度** ：12～14米/秒

**发射方向** ：（X：0，Y：0，Z：1）

**最大偏移角度** ：33

**起始色** ：RGB 值（255,102,0）

**终止色** ：RGB 值（255,255,255）

**生存时间** ：1～2秒

![](img/ParticleFire.gif) 
---- 
烟雾 |

**高度模式** ：绝对高度

**位置** ：（X，Y，Z)随机取值

**缩放** ：(X：1， Y：1， Z：1)

**粒子高度** ：10

**粒子宽度** ：10

**布告板模式** ：标准点布告板

**启用颜色渐变** ：Alpha 值=-12，RGB 值（-12，-12，-12）

**启用大小缩放率：** 5

**其他影响器作用** ：默认状态是关闭的

**发射频率** ：7个/秒

**初速度** ：8～10米/秒

**发射方向** ：（X：0，Y：0，Z：1）

**最大偏移角度** ：20

**起始色** ：RGB 值（163,163,163）

**终止色** ：RGB 值（163,163,163）

**生存时间** ：12～20秒

![](img/Smoke.gif) 
--- 
喷泉 |

**高度模式** ：绝对高度

**位置** ：（X，Y，Z)随机取值

**缩放** ：(X：1， Y：1， Z：1)

**粒子高度** ：1

**粒子宽度** ：1

**布告板模式** ：标准点布告板

**启用静态作用力** ：大小：10，作用方式：叠加，作用方向：（X：0，Y：0，Z：-1）

**启用反射面：** 反射率：10，放射方向：（X：0，Y：0，Z：1）

**其他影响器作用** ：默认状态是关闭的

**发射频率** ：800个/秒

**初速度** ：14～17米/秒

**发射方向** ：（X：0，Y：0，Z：1）

**最大偏移角度** ：2

**起始色** ：RGB 值（255,255,255）

**终止色** ：RGB 值（232,239,244）

**生存时间** ：2～5秒

![](img/Fountain.gif) 
--- 
爆炸 

**高度模式** ：绝对高度

**位置** ：（X，Y，Z)随机取值

**缩放** ：(X：1，Y：1，Z：1)

**粒子高度** ：15

**粒子宽度** ：15

**布告板模式** ：标准点布告板

**启用颜色渐变** ：Alpha 值=-37，RGB 值（-15，-15，-15）

**其他影响器作用** ：默认状态是关闭的

**发射频率** ：2000个/秒

**初速度** ：18～18米/秒

**发射方向** ：（X：0，Y：0，Z：1）

**最大偏移角度** ：90

**起始色** ：RGB 值（255,150,0）

**终止色** ：RGB 值（255,150,0）

**生存时间** ：0.3～1.5秒

**持续时间** ：0.2～0.2秒

**重启时间** ：0.1～3秒

![](img/Explode.gif) 
--- 
烟火 

**高度模式** ：绝对高度

**位置** ：（X，Y，Z)随机取值

**缩放** ：(X：1， Y：1， Z：1)

**粒子高度** ：11

**粒子宽度** ：11

**布告板模式** ：标准点布告板

**启用颜色渐变** ：Alpha 值=0，RGB 值（-50，-70，-50）

**启用大小缩放** ：20

**其他影响器作用** ：默认状态是关闭的

**发射频率** ：53个/秒

**初速度** ：21～31米/秒

**发射方向** ：（X：0，Y：0，Z：1）

**最大偏移角度** ：24

**起始色** ：RGB 值（204,204,0）

**终止色** ：RGB值（204,204,255）

**生存时间** ：3～3秒

![](img/FireSmoke.gif)  
---
烟花 

**高度模式** ：绝对高度

**位置** ：（X，Y，Z)随机取值

**缩放** ：(X：1， Y：1， Z：1)

**粒子高度** ：55

**粒子宽度** ：22

**布告板模式** ：Y轴旋转布告板

**启用颜色渐变** ：Alpha 值=0，RGB 值（-50，-50，-50）

**其他影响器作用** ：默认状态是关闭的

**多发射器**

**发射频率** ：1000个/秒

**初速度** ：80～150米/秒

**发射方向** ：（X：0，Y：0，Z：-1）

**最大偏移角度** ：180

**起始色** ：RGB 值（255,0,0）

**终止色** ：RGB 值（255,0,255）

**生存时间** ：1.5～1.5秒

**持续时间** ：0.1～0.1秒

**重启时间** ：2～2秒

![](img/Fireworks.gif)  
---
尾焰 

**高度模式** ：绝对高度

**位置** ：（X，Y，Z)随机取值

**缩放** ：(X：1， Y：1， Z：1)

**粒子高度** ：8

**粒子宽度** ：8

**布告板模式** ：Y 轴旋转布告板

**启用静态作用力** ：大小，10；作用方式，叠加

**启用颜色渐变** ：透明度，0；红，-50；绿，-50；蓝，-50

**其他影响器作用** ：默认状态是关闭的

**发射频率** ：600个/秒

**初速度** ：20～80米/秒

**发射方向** ：（X：0，Y：-100，Z：0）

**最大偏移角度** ：1

**起始色** ：RGB 值（255,102,0）

**终止色** ：RGB 值（255,255,255）

**生存时间** ：0.1～0.3秒

![](img/TailFire.gif) 
--- 
降雨 

**高度模式** ：绝对高度

**位置** ：（X，Y，Z)随机取值

**缩放** ：(X：1， Y：1， Z：1)

**粒子高度** ：30

**粒子宽度** ：20

**布告板模式** ：Y 轴旋转布告板

**启动随机作用力** ：大小，100；粒子比例，100

**其他影响器作用** ：默认状态是关闭的

**发射频率** ：2000个/秒

**初速度** ：300～300米/秒

**发射方向** ：（X：20，Y：20，Z：-100）

**起始色** ：RGB 值（255,255,255）

**终止色** ：RGB 值（255,255,255）

**生存时间** ：5秒

![](img/Rain.gif)  
---
降雪 

**高度模式** ：绝对高度

**位置** ：（X，Y，Z)随机取值

**缩放** ：(X：1， Y：1， Z：1)

**粒子高度** ：20

**粒子宽度** ：20

**布告板模式** ：Y 轴旋转布告板

**启用随机作用力** ：大小，200；粒子比例，100

**其他影响器作用** ：默认状态是关闭的

**发射频率** ：1000个/秒

**初速度** ：150～150米/秒

**发射方向** ：（X：0，Y：0，Z：-100）

**起始色** ：RGB 值（255,255,255）

**终止色** ：RGB 值（255,255,255）

**生存时间** ：6秒

![](img/Snow.gif)  
---
  
###  相关主题

 [粒子对象的创建](GeoParticleSetting)



