# CSSDemos
## 圣杯布局和双飞翼布局的不同
圣杯布局和双飞翼布局解决的问题是一样的，都是两边定宽，中间自适应的三栏布局，中间栏要在放在文档流前面以优先渲染。
* 两种方法基本思路都相同：首先让中间盒子 100% 宽度占满同一高度的空间，在左右两个盒子被挤出中间盒子所在区域时，使用 margin-left 的负值将左右两个盒子拉回与中间盒子同一高度的空间。接下来进行一些调整避免中间盒子的内容被左右盒子遮挡。
* 主要区别在于 如何使中间盒子的内容不被左右盒子遮挡：
 + 圣杯布局的方法：设置父盒子的 padding 值为左右盒子留出空位，再利用相对布局对左右盒子调整位置占据 padding 出来的空位；
 + 双飞翼布局的方法：在中间盒子里再增加一个子盒子，直接设置这个子盒子的 margin 值来让出空位，而不用再调整左右盒子。
 简单说起来就是双飞翼布局比圣杯布局多创建了一个 div，但不用相对布局了，少设置几个属性。
