# Talon 1400 固定翼无人机

个人独立项目 · 基于 [Flightory Talon 1400](https://flightory.com/product/talon-1400) 开源固定翼机型改造

## 项目概览

机身通体采用发泡材料 3D 打印成型，搭载 SpeedyBee 飞控、WalkSnail 图传与摄像头。

![3D CAD exploded view](3D%20CAD%20exploded%20view.png)
*机身 CAD 爆炸视图*

## 制作过程

![Fuselage in progress](Fuselage%20in%20progress.jpg)
*机身打印/组装中*

![Fuselage complete](Fuselage%20complete.jpg)
*机身完成*

![Adding some color schemes](Adding%20some%20color%20schemes.jpg)
*涂装配色*

![Paintjob complete](Paintjob%20complete.jpg)
*涂装完成*

![Front assembly](Front%20assembly.jpg)
![Front assembly complete](Front%20assembly%20complete.jpg)
*机头组装*

## 航电系统

搭载 SpeedyBee 飞控 + WalkSnail 数字图传系统与摄像头：

![Setting up flight controls](Setting%20up%20flight%20controls.jpg)
*飞控系统调试*

**视频：** [Camera mount ready.mp4](Camera%20mount%20ready.mp4) — 摄像头安装座就位

## 首飞与失效分析

![Ready for takeoff!](Ready%20for%20takeoff!.jpg)
*准备起飞*

**视频：** [Waaay too much power.mp4](Waaay%20too%20much%20power.mp4) — 动力系统测试，油门量偏大

**视频：** [Liftoff!!! Crashes immediately.mp4](Liftoff!!!%20Crashes%20immediately.mp4) — 首飞即坠毁

![Unfortunate ending](Unfortunate%20ending.jpg)
*坠毁后的机身*

**失效原因分析：** 坠落是由于起飞时油门给量过大，导致瞬时扭力过高，3D 打印材料在对应受力部位承受了过大的剪切力而断裂。

**解决方案：** 起飞前预先设定好合理的油门爬升曲线，避免瞬时大扭力；同时针对受力集中的部位在打印时局部提高填充密度，提升该区域的抗剪切强度。

## 我的角色

独立完成机身 3D 打印设计与制作、航电系统安装调试、试飞测试；试飞失效后独立完成失效原因分析（扭力-剪切关系判断），并提出油门曲线限制 + 局部密度强化的双重解决方案。
