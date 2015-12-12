# flexible的使用
##1、首先要明确的是rem单位的用法和特点
rem根据html根元素的font-size来换算，1rem=1根元素。
rem随着根元素变化而缩放，所以在flexible里就是用这个特点来换算的
##2、还有一个要明确的就是meta的initial-scale的缩放，这个也是flexible利用的一个重要的关键（这个知识点可以去百度）。
#接下来
##flexible的实现原理
`````
设计图的（width/10=html的font-size）(即你要写的css)->
flexible的font-size（根据屏幕大小和dpr换算出来的）（html的font-size=width*dpr/10）->
等比缩放的rem，把你的设计图等比缩放成了适应屏幕大小的页面
```
`````
根据dpr的数值来等比缩放页面initial-scale->
改变html的font-size,达到等比缩放->
两次等比缩放得到适应的页面，解决了1px的bug
```
###注意：
####一、font-size的使用
我们在移动端布局，推荐不用rem对字体做改变，但是要用sass写个宏定义
如果对于需要改变的可以使用rem，只是不推荐。
#####我的工具是sublime text3的cssrem是大漠的w3cplus介绍的
