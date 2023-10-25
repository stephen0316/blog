---
title: processing学习笔记（一）
categories: 
  - 技术
toc: true
date: 2023-8-27
thumbnail: https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/%E6%8A%80%E6%9C%AF%201.png
---

### 框架

```c
//声明变量
int ...
float ...

//初始化，执行一遍
void setup(){
    初始化代码块
}

//重复执行
void draw(){
    重复运行代码块
}

//写函数
returntype functionname (parameters){ 
    // code
} 
```
代码从上往下运行，后画的图形在最上层，注意顺序
### 操作符
&&（逻辑与）：同时满足<br>||（逻辑或）：满意任一条件<br>！（逻辑非）：否定

### background
background（0）：0-255，代表灰度<br>background（0,0）：0-255，代表灰度和透明度<br>background（0,0,0）：0-255，代表RGB<br>background（0,0,0,0）：0-255，代表RGB，透明度

### 基础图形
line(x1,y1,x2,y2)：线段的两个端点坐标<br>rect(x,y,width,height)：定位点在左上角<br>ellipse(x,y,width,height)：1.X轴方向的位置；2.Y轴方向的位置；3.长轴；4.短轴；定位点在圆心<br>arc(x,y,width,height,start,stop)：角度的两种表示方式：1）PI 、2）radians（X）；PI/2=radians(90)<br>triangle(x1,y1,x2,y2,x3,y3)<br>quad(x1,y1,x2,y2,x3,y3,x4,y4)<br>bezier(x1, y1, cx1, cy1, cx2, cy2, x2, y2)

<img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/00.png" alt="00" width="400"/>

调整图形的原点：--Mode，例：rectMode（CENTER）<br>参数类型：CORNER、CORNERS、CENTER和RADIUS
<div align="center"><img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/image.png" alt="image" width="600"/></div>

### 基础语句
#### fill
同background，会影响至下一个fill前的所有的图像<br>noFill() 不填充
#### stroke
stroke(0,0,0) 控制描边颜色<br>noStroke() 取消描边<br>strokeWeight(X) 描边，X为描边大小<br>strokeCap(mode) 线条端点形式，mode：SQUARE（方形端点）、PROJECT（方形延伸端点）、ROUND（圆形端点）

#### random
random(x,y)，y>x，否则无效
#### constrain
constrain(x,y,z)<br>x：需要限制的参数<br>y：最小值<br>z：最大值<br>eg：constrain(r,0,255) ：Red色值范围（0,255）
#### noise
noise(x)：线性<br>noise(x,y)：平面<br>noise(x,y,z)：立体

<img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/w.png" alt="w" width="400"/>

#### translate
translate（x,y）改变坐标系原点的位置
#### frameRate
运行draw()时的速度，例：frameRate(30)意味着每秒30帧

#### map映射函数
y=map(x,a,b,A,B)：把x在(a,b)区间内的值，映射到(A,B)区间
<img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/e.png" alt="e" width="500"/>

#### abs

abs()求绝对值，abs(x)>=0

#### 三角函数
x=圆心.x + r * cos(t)<br>y=圆心.y + r * sin(t)<br>t为弧度，radians（t）可以将角度转化为弧度
#### 鼠标交互
mouseX，mouseY<br>eg：ellipse(mouseX,mouseY,100,100)<br>pmouseX，pmouseY：前一个鼠标坐标<br>mousePressed() 
#### 键盘交互
keyPressed()
### 内置变量
<img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/r.png" width="600"/><br>

### 媒体
1、在根目录新建文件夹“data”，拖入图片

2、引用图片：

```c
PImage pic;//声明变量，变量名只能以_或字母开头

void setup(){
    size(500,500);
    pic=loadIamge("picname.jpg");//引用图片
}
void draw(){
    background(pic)//将图片作为窗口背景
    image(pic,0,0,150,150);//(变量名,x,y,width,heigth)
    pic.resize(300,300);//改变图片尺寸

    tint(明度);
    tint(明度,透明度);
    tint(R,G,B);
    tint(R,G,B,透明度);
}

```
### 重复
#### while循环
while（布尔表达式）{ 操作指令 }<br>考虑：1、循环的初始条件；2、循环的终止条件；3、循环的操作指令
#### for循环
for（初始值；布尔表达式）{ 操作指令 }
### 向量
PVector(x,y,z)<br>L.x可以获取向量的x值，y，z同理
```c
PVector L; //声明一个向量
...
L=new PVector(10,10,10); //初始化
```
add（）、sub（）、mult（）、div（） 向量的加减乘除<br>mag（）计算向量的长度<br>normalize（）单位化向量
### 数组
> 数组是指具有相同数据类型的数据元素组成的集合。数组同样有数据类型，而且一个数组内只能同时存在一种数据类型

特点：数据按顺序成组，每个数据项都有下标，数据项位置可交换

```
int shuzu[];
```
```
int shuzu[]=new int [100];
```
```c
int shuzu[]={1,2,3,4,5};
```
遍历数组，获取数组大小：**数组名.length**<br>
**二维数组**

```
int shuzu[][]=new int[2][4] //2行4列
```
### 函数
自定义函数：返回值类型、函数名、参数										
```c
returntype functionname (parameters){ 
    // code
} 
```
参数：实参、形参<br>实参：传递给函数的数值<br>形参：函数定义中的括号内部的变量声明
### 对象和类
对象：具有数据、功能，能完成某个任务，是一个实体<br>类：具有共同特征的对象的集合<br>类的组成：名称、数据、构造函数、方法（函数）

- 名称：自定义，首字母大写
- 数据：一系列变量
- 构造函数：构造函数是一种特殊的函数，位于类的内部，用于创建对象本身的实例，对变量进行赋值。当有一个新的对象从类中创造出来的时候，它具有和类相同的名字，用new运算符进行调用: Car myCar = new Car() 
- 函数：通过对函数功能的设置，为对象增加自定义函数 
#### 定义类：class
<img src="https://savemyblogpic-1311313070.cos.ap-chengdu.myqcloud.com/blogpicture/q.png" alt="q" width="400"/><br>

#### 创建对象
1. 声明一个对象<br>类的声明与变量类似，不同的地方是这里的变量类型是类的名称，后面的变量名是我们自定，另外对象不是初始值，而是一种复杂的数据类型
2. 初始化<br>声明完变量后会给其赋值，比如: x = 1;<br>初始化对象相对复杂一些，和赋值不同，需要通过 new 运算符构建这个对象，eg：lion=new Animal()
3. 调用对象的方法<br>当声明并初始化一个对象变量之后，就可以使用这个对象了。使用对象需要调用内置于对象之中的函数：

```c
variableName.objectMethod(method arguments); 
// eg：lion.display();
```

```c
Animal monkey; //声明对象
Animal lion;

void setup(){
  monkey=new Animal(100,100,100);//初始化
  lion=new Animal(0,0,0);
}

void draw(){
  monkey.函数名();//调用对象的方法
  lion.函数名();
}

class Animal{
 int x,y,z;//声明变量
 
 Animal(){ // 变量赋值
  x=
  y=
  z=
 }
    
 void 函数名(){
  ...
 }
    
}

```


 				
 			
 		
 	 

