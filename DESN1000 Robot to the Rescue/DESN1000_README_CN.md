# DESN1000 履带式搜救机器人 "Wall-F"

新南威尔士大学大一《工业设计与加工制造》课程（DESN1000）小组项目 · **年级第一作品**

## 项目任务

设计一台可以在模拟灾后地形中移动、通过超声波雷达扫描地形建图、并抓取"幸存者"（网球）的搜救机器人。

## 我的角色

CAD 设计、加工制造、硬件迭代、软件结构设计与测试。

## 设计历程 — Version 1.0

从概念草图开始，确定履带式底盘方案：

![Concept drawing](Concept%20drawing.jpg)
*概念草图*

![Tank drive design of version 1.0](Tank%20drive%20design%20of%20version%201_0.jpg)
*V1.0 履带驱动机构设计*

**最大的成本创新**：没有用现成的橡胶履带（成本高、课程预算有限），而是用激光切割的尼龙布做履带连接件，再用透明鱼线把 3D 打印的履带板逐块缝合起来——把整套履带系统的制作成本压到 **5 澳元以内**，是本课程历年最低成本的履带式方案。

![Sewing together the tank tracks](Sewing%20together%20the%20tank%20tracks.jpg)
*用鱼线缝合3D打印履带板*

![Still sewing tank tracks](Still%20sewing%20tank%20tracks.jpg)
*履带缝合过程*

![Tank tread prototype](Tank%20tread%20prototype.jpg)
*履带板原型*

![Tank tread tensioning system prototype](Tank%20tread%20tensioning%20system%20prototype.jpg)
*履带张紧系统原型*

![Tank tracks complete](Tank%20tracks%20complete.jpg)
*完整履带组件*

![Tank drive components](Tank%20drive%20components.jpg)
*履带驱动组件*

![Version 1.0 chassis](Version%201_0%20chasis.jpg)
*V1.0 底盘*

![Version 1.0 complete](Version%201_0.jpg)
*V1.0 整车*

**演示视频：** [Design montage of version 1.0.mp4](Design%20montage%20of%20version%201_0.mp4)

## 感知与软件架构

全车采用高度模块化设计，方便快速迭代和更换应用场景。软件结构采用分部处理：

- **车载 Arduino**：记录超声波雷达和 IMU 数据，通过蓝牙模块传递给电脑；控制抓取机构抓取"幸存者"网球；控制两侧电机转向
- **车载 ESP32 摄像头**：通过 WiFi 传输实时画面
- **电脑端**：根据蓝牙回传的超声波雷达和角度数据重建地形地图，自动生成路径规划，向 Arduino 发送两侧电机转动指令；接收 WiFi 视频画面

![IR capture logic 1](IR%20capture%20logic%201.jpg)
![IR capture logic 2](IR%20capture%20logic%202.jpg)
![IR capture logic 3](IR%20capture%20logic%203.jpg)
*红外/抓取逻辑设计*

![Front assembly prototype](Front%20assembly%20prototype.jpg)
*前端抓取机构原型*

![Omni adaptor panel](Omni%20adaptor%20pannel.jpg)
*全向轮适配面板*

## 设计历程 — Version 2.0 "Wall-F"

在 V1.0 基础上迭代出结构更完整的 V2.0：

![Version 2.0 CAD prototyping](Version%202_0%20CAD%20prototyping.jpg)
*V2.0 CAD 原型设计*

![Version 2.0 CAD complete](Version%202_0%20CAD%20complete.jpg)
*V2.0 CAD 完整模型*

![Version 2.0 chassis complete](Version%202_0%20Chasis%20complete.jpg)
*V2.0 底盘完成*

![Wall-F Version 2.0](Wall-F%20Version%202.0.jpg)
![Wall-F Version 2.0 closeup](Wall-F%20Version%202.0%20closeup.jpg)
![Wall-F Version 2.0 is live](Wall-F%20Version%202.0%20is%20live.jpg)
*Wall-F V2.0 整车与细节*

**演示视频：** [She moves!!!!.mp4](She%20moves!!!!.mp4)
