# Voron 2.4 "Pinky" — CoreXY 3D 打印机搭建与四驱升级

个人独立项目 · 基于开源项目 [Voron](https://vorondesign.com) 改造

![Pinky's full view](Pinky%27s%20full%20view.jpg)
*"Pinky" 整机*

## 项目概览

从最基础的材料采购开始，机架搭建、电路设计、电子元件选配、CAN 总线通讯配置、打印机固件编写、运动调试与共振检测补偿，全部由个人独立完成。

![Bare Al frame](Bare%20Al%20frame.jpg)
*铝型材机架搭建*

## 电子系统

![Electronics bay view](Electronics%20bay%20view.jpg)
*电控仓布局*

![Electronics layout](Electronics%20layout.jpg)
*电路布线*

## 四驱升级（All-Wheel-Drive）

标准 CoreXY 架构原本用两个步进电机驱动 X/Y 轴，我把它升级为四步进电机驱动（"四驱"），把打印速度提升到 **650mm/s**，移动速度提升到 **1000mm/s**。加速度方面，**45000mm/s² 是稳定可靠运行的数值**；测试中把加速度推到 55000mm/s² 也能勉强跑起来，但会开始出现下文提到的丢步问题，所以量产级参数以 45000mm/s² 为准。

驱动方案上，最初用的是 TMC2209 + TMC2240 组合，后续升级为 TMC5160 高压驱动，进一步提升了高加速度下的稳定性。

**演示视频：**
- [45000mms^2 acceleration.mp4](45000mms%5E2%20acceleration.mp4) — 加速度测试
- [12 min benchy.mp4](12%20min%20benchy.mp4) — 12分钟打印完成标准测试模型 Benchy
- [Infinite printers.mp4](Infinite%20printers.mp4) — 连续打印测试

## 自定义 MCU 与驱动器安装座

为了更好地组织电控走线、提升散热效果，自主设计了 MCU 与电机驱动器的安装支架：

![MCU and Motor driver stand drawing](MCU%20and%20Motor%20driver%20stand%20drawing.png)
*安装座工程图*

![MCU and Motor driver stand CAD](MCU%20and%20Motor%20driver%20stand%20CAD.jpg)
*安装座 CAD 模型*

![MCU and Motor driver stand](MCU%20and%20Motor%20driver%20stand%20.jpg)
*安装座实物*

![MCU and Motor driver stand with cooling fans](MCU%20and%20Motor%20driver%20stand%20with%20cooling%20fans.jpg)
*加装散热风扇后的安装座*

## 遇到的技术问题与排查

**问题一：静电堆积导致步进电机驱动器频繁报错**
运行中偶发的静电积累会导致步进电机驱动器（当时使用 TMC2240）报错停机。

**问题二：高加速度下主板串扰导致丢步**
使用的 STM32 主板在更高加速度设置下会出现高频信号串扰问题，导致步进电机丢步，这也是加速度参数最终定在 45000mm/s²（而非测试上限 55000mm/s²）的原因。

针对以上两个问题，自发整理了完整的技术报告发送至主板厂家，推动问题的确认与后续跟进排查。

## 我的角色

独立完成从机架搭建、电控设计、固件配置到故障诊断的全流程，包括四驱升级方案设计、自定义安装座设计、以及主板高频信号问题的诊断与厂商反馈。
