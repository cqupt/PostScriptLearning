*项目目的
----
		学习PostScript笔记
*项目地址
----
[地址](https://github.com/cqupt/PostScriptLearning)	

*目录结构:
---
>
> CHAPTER3----->BEGINNING GRAPHICS
> 
>CHAPTER4---->POSTSCRIPT DICTIONARIES
>

*树形结构
---

###
		│  .gitattributes
		│  .gitignore
		│  ch3_demo10_darw-a-overlapping-squre-again-with-procedure and inch.png
		│  Postscritpt-keyword.txt
		│  ReadMe.md
		│  summary-unit2.png
		│
		├─chapter3
		│  │  summary-unit3.png
		│  │
		│  ├─PDFoutput
		│  │      ch3_demo1_darw-line.pdf
		│  │      ch3_demo2_darw-two-line.pdf
		│  │      ch3_demo3_darw-a-squre.pdf
		│  │      ch3_demo4_darw-a-better-squre.pdf
		│  │      ch3_demo5_darw-a-better-squre.pdf
		│  │      ch3_demo5_darw-a-triangle.pdf
		│  │      ch3_demo6_darw-a-filled-squre.pdf
		│  │      ch3_demo7_darw-a-gray-squre.pdf
		│  │      ch3_demo8_darw-a-overlapping-squre.pdf
		│  │
		│  └─Source
		│          ch3_demo1_darw-line.ps
		│          ch3_demo2_darw-two-line.ps
		│          ch3_demo3_darw-a-squre.ps
		│          ch3_demo4_darw-a-better-squre.ps
		│          ch3_demo5_darw-a-triangle.ps
		│          ch3_demo6_darw-a-filled-squre.ps
		│          ch3_demo7_darw-a-gray-squre.ps
		│          ch3_demo8_darw-a-overlapping-squre.ps
		│
		└─chapter4
		    │  summary-unit4.png
		    │
		    ├─PDFoutput
		    │      ch4_demo1_darw-a-overlapping-squre-again-with-procedure.pdf
		    │      ch4_demo2_darw-a-overlapping-squre-again-with-procedure and inch.pdf
		    │
		    └─Source
			    ch4_demo1_darw-a-overlapping-squre-again-with-procedure.ps
			    ch4_demo2_darw-a-overlapping-squre-again-with-procedure and inch.ps


*示例代码
---
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
---
![Test XIB](https://raw.github.com/cqupt/PostScriptLearning/master/ch3_demo10_darw-a-overlapping-squre-again-with-procedure%20and%20inch.png)