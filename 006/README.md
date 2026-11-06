# 阿哈课程与创客项目研究报告 第006期

**日期：2026-10-23**  
**主题：开源3D扫描、动态沙画与机械互动**

> Markdown线上归档版。本页仅整理已在对话中确认的主要项目与建议；正式DOCX中的全部来源、BOM和许可细节尚未逐项转录。不能把本页当作完整研究报告。

## 决策摘要

优先验证低成本、可复制且与现有3D打印/激光切割/ESP32或micro:bit设备匹配的项目。未实测成本、年龄、课时和可靠性均为规划假设。

## A. 课程研发项目

### PixelIt

ESP32像素矩阵显示、JSON控制；建议9–15岁、4–6课时。WLED与PixelIt是不同固件，不能直接混用。

原始资料/检索入口：[打开链接](https://github.com/pixelit-project/PixelIt)

### OpenScan Mini

树莓派、步进电机、摄像头的摄影测量扫描仪；建议12岁以上、6–12课时。先核实硬件版本及成像精度。

原始资料/检索入口：[打开链接](https://openscan.eu/pages/openscan-mini)

### Sandify

数学轨迹生成工具，可导出G-code；建议10岁以上、2–10课时。完整沙画机另需机械控制方案。

原始资料/检索入口：[打开链接](https://github.com/jeffeb3/sandify)

### 4-port USB Hub

实用电子产品设计，USB集线器、3D打印与焊接；建议12岁以上、2–3课时。

原始资料/检索入口：[打开链接](https://learn.adafruit.com/4-port-usb-hub-for-ikea-mittzon-desk)


## B. 灵感库与高阶观察

### Spider Candy Box

机械弹出盒，商业授权待核。

原始资料/检索入口：[打开链接](https://makerworld.com/en/models/640947-halloween-trick-or-treat-spider-candy-box)

### Bezalel

机械触觉显示器，另有专利限制需要核实。

原始资料/检索入口：[打开链接](https://github.com/pedrosacramento/bezalel)


## 本周课程开发计划

P0：ESP32 16×16 LED矩阵稳定运行和供电温升测试；P0：原创机械弹出盒30次可靠性测试；P1：Sandify三种曲线轨迹模拟。

## 核查与停止条件

先核查原始作者、代码和CAD文件、BOM、商业许可与供电/运动安全；如关键文件缺失、成本超出预算或样机重复测试失败，暂停正式课程开发。
