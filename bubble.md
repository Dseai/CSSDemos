请用CSS实现如下图的样式，相关尺寸如图示，其中dom结构为：
&lt;div id=”demo”&gt;&lt;/div>
![](http://i.imgur.com/VMnETJk.png)
    
    #demo {
    width: 100px;
    height: 100px;
    border: 2px solid #000;
    position: relative;
    }
    #demo:after {
    content: '';
    display: block;
    width: 14.1421px;
    height: 14.1421px;
    border-top: 2px solid #000;
    border-right: 2px solid #000;
    position: absolute;
    right: -10px;
    top: 20px;
    transform: rotate(45deg);
    background-color: #fff;
    }
>解题思路：
>
1. 将三角形用一个正方形来实现
2. 设置其上border,右border的宽度
3. 设置其背景颜色为白色以覆盖掉父元素的border
4. 使用transform: rotate 来让该正方形旋转
5. 使用top,left来对其定位