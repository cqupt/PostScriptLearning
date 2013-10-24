*学习PostScript笔记
=====
*项目地址
=====
[地址](https://github.com/cqupt/PostScriptLearning)	

*示例代码
=====
``` 
% ------- Define procedures----

/inch {72 mul} def   %这样的话,就可以直接指定多少英寸了.

/box	 % stack: x y => ---
{ 
newpath moveto		%定位起点

1 inch 0 rlineto	%右
0 1 inch rlineto	%上
-1 inch 0 rlineto	%左
closepath 		%封闭:下

} def


/fillbox % stack: grayvalue => ---
{ 
setgray 		%灰度设置
fill 			%填充
} def


% ----------- Main Program -----------

3.5 inch 4.5 inch box   % 定位:坐标(3.5,4.5)英寸,然后绘制一个矩形
0 fillbox		%根据指定灰度填充

4 inch 5 inch box
.4 fillbox

4.5 inch 5.5 inch box
.8 fillbox

showpage
``` 
示例结果:
=====
![Test XIB](https://github.com/cqupt/PostScriptLearning/blob/master/ch3_demo10_darw-a-overlapping-squre-again-with-procedure%20and%20inch.png?raw=true)