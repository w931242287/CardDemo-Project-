# CardDemo-Project-
本工程使用Unity 2020.1.17创建，低版本可能打不开。

Unity引擎的界面，左边是一个列表用来放场景里所有存在的Object，下面是你的库存，右边是点开每个具体object的属性窗口

Unity总体的编写思路就是给Object绑定一个脚本。

object分两种，一种是从prefab（库存里有对应文件夹），相当于从一个模板创建；另一种是无模板的单独个体，适用于该object独一无二。从prefab的创建的object，在左侧列表中显示为蓝色。

一开始不存在于左侧列表，后期再生成的object，需要从prefab实体化，对应的函数是instantiate。工程里的卡牌都是这样创建的。

绑在object上的脚本，可以看到几乎都定义了很多public类gameobject变量。这样定义之后可以在该object的右侧属性窗口里，把某个prefab或者左侧列表里的object拖到script框下，指定为这个变量。比如说我要生成卡牌并把他归到手牌区的父类之下，要给卡牌脚本指定哪个object是手牌区，就需要这样定义。记得脚本里这些gameobject变量都有所指代的，怕你们不理解。

UI的功能比较复杂，涉及到很多值传递啥的，我写的都比较暴力（搞了一大堆静态变量）。我在每个代码里就写了不少注释的，在github页面打开Assets/Script文件夹，我还给每个代码是干嘛的写了描述orz但还是很乱，反正不懂就问我！
