# 阿哈课程与创客项目研究报告 第008期

> 阅读版：保留原报告的项目分析与研发建议，已将文献编号改为可直接点击的来源链接。原Word表格转换为逐行文本，后续可继续优化排版。

阿哈课程与创客项目深度研究报告 #008  
  
阿哈 | 开源 Maker 与课程研发周报  #008  
  
  
  
RESEARCH BRIEF  /  008  
阿哈课程与创客项目  
深度研究报告  
从开源项目到可复现的课堂产品  
  
  
检索周期  2026-10-30 — 2026-11-06（含本周新报道与跨期经典补挖）  
资料核查日  2026-11-06  
本期入选  6项：4项课程研发候选，2项技术观察与灵感项目  
本期核心决策  先验证“低龄纸板音乐硬件 + 激光切割排版”，再安排模块化输入设备与流体仿真样机。  
  
  
  
	决策层级  
	建议动作  
	当前证据边界  
  
	P0 / 立刻验证  
	micro:bit 纸板电吉他；Nestbolt 激光排样  
	无需采购复杂新设备；先做教案与加工试验  
  
	P1 / 教师样机  
	ESP32-S3 流体模拟灯；Suutari20 模块化控制台  
	有源码/制造入口；尚无本团队硬件复现  
  
	观察 / 暂不采购  
	XGO Duck；IronEar  
	许可和版本/发布成熟度仍是阻断条件  
  
  
  
阅读说明：文内「已核实」仅表示官方网页/仓库可核验；「作者自述」不是独立实测；「研发建议」为阿哈拟采用的课程假设。成本与课时均非课堂实际记录。  
  
  
目录 / 阅读导航  
## 01 决策摘要与本周新变化   /   p.2  
02  筛选方法与取舍矩阵   /   p.3  
## 03 A类：直接课程研发项目   /   p.3  
    A1  micro:bit 纸板电吉他   /   p.3  
    A2  Nestbolt 开源激光排样   /   p.3  
    A3  ESP32 8×8 流体模拟   /   p.4  
    A4  Suutari20 模块化宏键盘   /   p.4  
## 04 B类：创客灵感与技术观察   /   p.5  
    B1  XGO Duck 具身智能双足鸭   /   p.5  
    B2  IronEar 端侧声音识别   /   p.5  
## 05 四周课程开发与验收条件   /   p.5  
## 06 开源商业许可与风险清单   /   p.6  
## 07 原始证据与资源索引   /   p.6  
页码在每页页脚；目录链接可从PDF或Word跳转至相应章节。原始网页链接均以编号[Sxx]呈现，见末尾可点击索引。  
## 01 决策摘要与本周新变化  
本期不追求“更多项目”。按制造文件可得性、低龄课堂完成度、长期升级链、安全风险及商业复用确定6项重点。上期已研究的普通LED像素灯、桌面宠物、沙画和3D扫描，本期不重复推荐。  
关于“本周新”的日期判断  
	主题  
	可确认日期  
	准确表述  
  
	IronEar  
	2026-11-03 业内报道；仓库于10月已存在  
	本周被报道；并非确认本周首次开源，硬件/固件尚待阶段性发布  
  
	XGO Duck  
	2026-11-01 业内报道；初次公开于9月左右；运行仓库11月5日显示更新  
	是本周报道/活跃项目，不是本周首次发布  
  
	Nestbolt  
	作者文档披露11月5日对外部客户端连接验证  
	本周有新的验证说明，工具核心已在此前开发  
  
	Suutari20  
	2026-10-31再次报道；原维基2025年已存在  
	本周重新发现，非新发布  
  
	micro:bit Guitar / ESP32 Fluid  
	经典教学资源/长期存在的开源仓库  
	本期补挖；未宣称本周首发  
  
  
  
决策结论  
先做 micro:bit 纸板吉他：制作可视、低成本增量、2节课即可形成可展示成果，教师故障排查相对简单。  
把 Nestbolt 用于激光切割节材试教：不急着部署MCP；先拿相同零件比较手工排版与软件排版，记录废料率和切割尺寸。  
ESP32流体仿真作为中高龄研发项目：确认板卡型号、功耗和实际帧率；暂不承诺零基础学生当堂完成。  
Suutari20的“物理模块/USB HID/自定义”价值高，但需焊接、PCB和QMK调试，不宜直接做低龄招生体验课。  
XGO Duck与IronEar的展示价值强；前者原始设计授权未定，后者关键硬件/固件未完全发布，均暂缓批量采购。  
02  筛选方法与取舍矩阵  
筛选依次检查：①原始作者与时间；②源码、BOM、CAD/STL/板图、装配；③实际课堂故障点；④材料预算和设备负担；⑤代码/模型/文档/图片许可；⑥是否有基础版到高阶版的课程升级链。评分不以热度或星数替代实际证据。  
	项目  
	材料/代码  
	低龄适配  
	教师投入  
	结论  
  
	micro:bit Guitar  
	官方教程+MakeCode/Python；纸板可自制  
	高（8+）  
	低  
	P0：2—4课时  
  
	Nestbolt  
	软件仓库+文档+实例，MIT  
	中（11+）  
	低—中  
	P0：3—5课时/工坊  
  
	ESP32 Fluid 8×8  
	源码+外壳+用户手册，MIT  
	低（12+）  
	中—高  
	P1：6—8课时  
  
	Suutari20  
	PCB/KiCad/Gerber/外壳+QMK，MIT  
	低（12+）  
	高  
	P1：6—10课时  
  
	XGO Duck  
	BOM/装配/3D+运行项目，授权分层  
	教师/高中  
	很高  
	B：先技术评审  
  
	IronEar  
	模型公开；硬件/固件阶段发布  
	教师/高中  
	很高  
	B：等待文件齐备  
  
  
  
预算口径：后续出现的人民币金额属于“内部预研采购上限提案”，非经供应商报价或实测产生的市场成本；不含人工、设备折旧、物流税费。上限若超出，应重新分解BOM后审核。  
## 03 A类：直接课程研发项目  
### A1 micro:bit 纸板电吉他 | 最快成课  
已核实的原始资料  micro:bit 教育基金会提供纸板/铝箔/鳄鱼夹的电吉他教程，支持 MakeCode 与 Python，含可下载程序；课堂内容采用 CC BY-SA 4.0。另有 Scratch 吉他路线及音高/八度进阶。  
硬件/原始文件  micro:bit（推荐V2）、鳄鱼夹、纸板、铝箔、胶带、可选电池与扬声器。无需第三方STL或PCB；官方教程/代码已可用，DIY外观由阿哈原创。  
复现难点与边界  不同板卡和电极接触会导致触摸触发差异；旧版V1外放声音须外接设备；Scratch方案依赖电脑与Scratch Link。注意音量和剪刀/裁纸刀监管。  
成本/教师负担  内部上限提案：已有micro:bit时耗材≤40元/组；新增板卡时整组≤300元（2026-11-06规划目标，不是市场报价）。准备1—2小时即可完成一版样机与预切纸板。  
课程设计  8—12岁；2节体验，4节标准。第1节制作乐器与触摸电路；第2节编辑音符/音色并演奏；第3节变量与节奏；第4节英语介绍作品与演出。  
升级树  Scratch/MakeCode触摸事件 → Python函数与列表 → 频率/倍频（440Hz→880Hz） → 加入角度传感器控制音高 → CAD/激光切割原创乐器壳。  
验收/停止条件  每个小组3分钟内成功触发3个不同音符；20次触摸触发≥18次；教师能在5分钟内定位鳄鱼夹/接地故障。若过度依赖电脑配置，改用板载声音版本。  
原始证据  [micro:bit 触摸吉他](https://www.microbit.org/projects/make-it-code-it/guitar-1-touch-tunes/) · [micro:bit 音程升级](https://www.microbit.org/projects/make-it-code-it/guitar-3-octaves/)  ·  [Scratch 吉他](https://www.microbit.org/projects/make-it-code-it/scratch-guitar/)  
### A2 Nestbolt | 激光切割排样与节材课程  
已核实的原始资料  开源Rust/WebAssembly排样工具，支持SVG/DXF输入、多板材、旋转和间距约束，提供浏览器版、CLI与MCP；MIT许可并披露第三方依赖。作者发布了冻结版本基准测试和11月5日客户端连通性说明。  
本期核心价值  不仅是“好用的软件”，更可把面积计算、二维排样、材料浪费、工程约束与激光切割连接起来。学生完成相同零件的手排/自动排版对照，而不是只做理论测算。  
原始文件与门槛  源码、Web应用、命令行、示例SVG/DXF、许可证、基准报告齐备；不是完整机器制作项目，不涉及新电子硬件。必须检查激光器自身加工格式、焦点、边缘留量与热影响区。  
真实性警戒  作者称冻结基准在部分任务上材料节约中位数为8.5%（60s），这是作者测试，不等于阿哈现场节材率；应以自身图形和板材复验。浏览器主分支可能比稳定版新，记录具体版本。  
成本/课程  软件授权成本0元（MIT）；使用现有激光设备，板材费用按实际消耗另核。11—16岁，建议3—5课时：手工排版→面积/间距→软件排样→激光验证→计算节材率。  
升级树  矩形装箱 → 非规则轮廓排样 → 激光切缝kerf/禁入区 → CAD/矢量设计 → Python批量生成SVG → 高中算法/组合优化与AI工具调用。  
验收/停止条件  同一套≥15件零件在纸上及软件排样；导出的1:1尺寸无比例变化；真实切割后检验至少5处配合尺寸；能解释为什么某些算法排样反而不优。若实切几何不符合预期，暂停使用该输出作为生产刀路。  
原始证据  [Nestbolt 源码](https://github.com/skulitom/Nestbolt) · [Nestbolt 演示](https://skulitom.github.io/Nestbolt/)  ·  [Nestbolt 依赖声明](https://github.com/skulitom/Nestbolt/blob/main/THIRD_PARTY_NOTICES)  
### A3 ESP32-S3 8×8流体仿真 | 物理×互动艺术  
已核实的原始资料  作者公开PlatformIO工程、源码、3D外壳文件、使用手册与MIT许可证；目标硬件为Waveshare ESP32-S3-Matrix（64颗LED及QMI8658 IMU），通过倾斜改变模拟重力。采用FLIP/PIC思路。  
教学价值  有别于上期普通像素灯：核心是“物理模型随重力方向变化”。低阶理解粒子、速度、重力、碰撞；中阶探索2D数组、坐标、插值；高阶分析FLIP与PIC混合、压力投影、性能与能耗。  
复现障碍  依赖特定Waveshare ESP32-S3-Matrix板载引脚；资料列出GPIO14/11/12等，替代开发板不能直接套用；内置电池/充电板/外壳增加焊接和锂电安全风险。  
成本/课程  内部教师样机上限建议350元/套（未询价）；学生第一阶段仅用USB供电，不装锂电。12—16岁，6—8课时；初阶课程可先用电脑模拟粒子运动再移植硬件。  
升级树  固态LED点阵 → IMU姿态 → 模拟粒子 → 重力/摩擦参数 → Python数值可视化 → C++性能优化和模型误差分析。英语用于阅读工程注释和材料说明。  
验收/停止条件  USB供电下连续30分钟稳定显示；四方向倾斜与重力响应一致；编译环境可从干净PC复建；记录平均帧率和温升。若性能明显抖动或依赖未锁定，不进常规教学。  
原始证据  [ESP32 Fluid 源码](https://github.com/Vateva/Esp32FluidSimulation8x8) · [ESP32 Fluid 外壳](https://github.com/Vateva/Esp32FluidSimulation8x8/tree/main/Casing%20and%20box)  ·  [ESP32 Fluid 手册](https://github.com/Vateva/Esp32FluidSimulation8x8/blob/main/8x8FluidSimulationUserManual.pdf)  
### A4 Suutari20 | 模块化控制台与可维修产品设计  
已核实的原始资料  原作者仓库有KiCad、Gerber、3D打印壳体、Vial固件目录与MIT许可证，README列出Raspberry Pi Pico、8个PJ-320A、热熔嵌件与螺钉，Wiki含Build Guide。10月31日是再报道日期，不是最初发布日。  
课程核心价值  标准3.5mm TS/TRS/TRRS接口让按键、旋钮等输入模块可拆换；作品能成为学生自己的画图/音乐/3D打印工具快捷控制台。符合维修、更换、模块化产品工程思想。  
核心障碍  需要定制PCB、焊接、掌握信号映射与QMK/Vial配置；Wiki仍存在“更多内容待补”的提示。不同TS/TRS/TRRS线序不可自行推断，必须以KiCad原理图和具体模块核查。  
成本/教学  内部P1打样预算上限450元/套（含少量试样PCB/按键/接口，未询价）。12岁以上，6—10课时；不建议零基础儿童直接焊接整套主板。  
升级树  按钮与USB-HID → 固定键映射 → 3.5mm插拔模块 → 旋钮/编码器 → CAD自制外壳 → 可维修性设计与标准接口分析。可加英语快捷命令、编程宏和数字媒体控制。  
验收/停止条件  至少2类模块可热插拔前先断电安全更换（不承诺带电热插拔）；50次插拔后功能仍正常；USB与供电无短路；课程化后可在10分钟内更换坏模块。  
原始证据  [Suutari20 源码](https://github.com/Squalius-cephalus/suutari20) · [Suutari20 装配](https://github.com/Squalius-cephalus/suutari20/wiki/Getting-started)  ·  [Suutari20 报道](https://www.open-electronics.org/suutari20-a-modular-macro-keyboard-built-on-3-5-mm-audio-jacks/)  
## 04 B类：创客灵感与技术观察  
### B1 XGO Duck | 15舵机双足机器人与神经策略  
项目定位  Luwu Dynamics基于Pollen Robotics Microduck机体重新设计电子系统，提供3D结构、PCB、BOM、装配手册与Arduino UNO Q运行项目。运行项目含步行/起身等策略，11月5日仓库仍有活动。原项目更早公开，非本周首发。  
值得研究  它连接机械装配、串行总线舵机、IMU、Linux+STM32分工、约50—100Hz控制回路与强化学习推理。可用作未来高中机器人实验室“仿真政策与实机控制的边界”专题。  
关键风险  官方LICENSING.md明确说明硬件仓库未形成单一完整许可证；部分原创材料意向为教育复制、商业另授权，且上游Microduck组件应独立审查。15舵机、锂电和双足稳定性使课堂成本、调试和安全风险很高。  
课程规划（条件性）  14岁以上，先1节公开视频与政策可视化，教师验证通过后考虑12—20节高阶班；不要为招生宣传许诺学生能直接训练出稳定步态。  
下一关口  完整材料清单和设备报价、授权范围书面确认、关节零位校准、跌倒/卡死保护、外壳质量与电池保护确认前，不进入采购。  
原始证据  [XGO Duck 硬件](https://github.com/LuwuDynamics/xgoduck_hardware) · [XGO Duck 许可](https://github.com/LuwuDynamics/xgoduck_hardware/blob/master/LICENSING.md)  ·  [XGO Duck 程序](https://github.com/LuwuDynamics/xgoduck_runtime_arduino) · [XGO Duck 报道](https://www.open-electronics.org/xgo-duck-the-open-source-robot-duck-that-walks-with-neural-policies/)  
### B2 IronEar | 端侧声音识别与隐私保护  
项目定位  2026-11-03业内报道了ESP32-S3+3路MEMS麦克风的端侧音频分类节点，拟通过MQTT/LoRa联动。作者称可识别YAMNet系521类声音；其众筹页面目前仍标注Coming Soon。  
开放状态需要准确区分  截至核查：模型权重/类别表已公开（Apache-2.0；类名CC BY）；固件预计发货前发布，原理图/BOM在众筹时发布，Gerber/STEP随交付发布；推理引擎源码与训练数据保持闭源。不能将整个项目表述为已完整开源、可立即复现。  
教学价值  可转化成“声音事件 vs 连续录音”的数据隐私讨论，识别噪声、门铃、动物叫声时分析误报/漏报，连接音频特征、数据集偏差、IoT自动化与安全。  
课程方案（前置研究）  14岁以上；先用现成微控制器/麦克风做离线声强或简单分类演示，不直接依赖未发布的IronEar整机。4—8节可扩展成TinyML实验，要求任何录音/数据采集经同意且不公开学生个人声音。  
成本/停止条件  众筹价格、整机电池续航及主要制造文件未发布，暂无法可靠报价；进入采购条件：关键文件/许可、量产版本、区域无线合规、端侧模型准确率与延迟验证齐备。  
原始证据  [IronEar 源码](https://github.com/PionEars/IronEar) · [IronEar 官方](https://www.crowdsupply.com/ironear-technologies/ironear)  ·  [IronEar 报道](https://www.open-electronics.org/ironear-the-privacy-first-audio-sensor-that-recognises-500-sounds-on-device/)  
## 05 四周课程开发与验收条件  
课程研发建议以小规模教师验证和真实试教作为门槛，不将推荐结论等同于已完成样机。下表是下一周期的工作安排，非已经执行的结果。  
	阶段  
	任务与交付物  
	通过标准  
	失败后的处理  
  
	W1 / P0  
	micro:bit 纸板吉他原型；2节试教提纲  
	3音符识别≥90%；外观与交互能完成  
	更换夹线/加大触摸片；优先V2离线版  
  
	W1 / P0  
	Nestbolt 案例，15件零件排样试验  
	SVG尺寸100%吻合；按真实板材切割  
	回退人工/传统CAM；检查间距/比例  
  
	W2 / P1  
	ESP32流体仿真教师样机  
	30min稳定、IMU四向响应、记录FPS  
	锁定板卡版本；退回电脑模拟  
  
	W2—W3 / P1  
	Suutari20 PCB/壳体/输入模块  
	完成两种模块、50次插拔、USB安全  
	先改成面包板宏键盘过渡版  
  
	W3  
	微型试教、家长观察、材料和返工记录  
	≥80%学生能解释核心原理并展示作品  
	拆短活动、保留样机观摩模式  
  
	W4  
	课程母库入库审查  
	教师手册、BOM、授课目标、许可表齐全  
	延后入库；保留研究候选  
  
  
  
建议的教师材料包规范  
每个项目交付：视频演示、硬件BOM及采购版号、STL/CAD来源、程序Commit SHA/版本号、接线表、调试日志、教学PPT/任务单、适龄/安全说明。  
每个项目至少制作：体验课（最快得到作品）、标准课（学生自主修改）、进阶课（使用Python/C++/AI或CAD深挖）的三层路径。  
AI辅助流程必须加入：提示词/生成代码 → 编译/复现 → 学生解释关键逻辑 → 故障注入 → 修改与回归测试；不能只让AI生成作品。  
入库评分与明确停损  
建议硬性门槛：教师独立复现可执行；危险能量、锂电、激光、快速运动具备控制措施；单组材料预算经供应商报价确认；第三方资源具备可用授权或已自行原创替代；试教中至少80%小组按课时完成主要动作。如果同一关键故障两轮仍无法在课时内恢复，转入教师展示库而非正式收费课程。  
## 06 开源商业许可与风险清单  
	项目/资产  
	核实情况  
	收费课程的执行要求  
  
	micro:bit 官方教程  
	教学网页注明CC BY-SA 4.0  
	署名和同方式共享改编教学内容；自制外观与课堂照片自行管理  
  
	Nestbolt  
	主项目MIT，列明依赖声明  
	保留MIT许可/第三方声明；现场切割仍由教师审定  
  
	ESP32 Fluid  
	仓库MIT；源码及外壳见仓库  
	保留归属与许可证；外购模块遵从供应商限制  
  
	Suutari20  
	仓库MIT；QMK/Vial等有独立许可  
	复制相应原始声明；审核固件依赖与商标  
  
	XGO Duck  
	硬件设计无项目统一完整许可；上游资产混用  
	商业复制/收费教材引用CAD前先逐文件授权，不推定默许可  
  
	IronEar  
	开放发布分阶段；推理引擎/训练资料闭源  
	不可视作完整开放硬件；谨慎处理隐私/无线许可  
  
  
  
合规补充：本报告仅为研发表，不能替代法律审查。尤其关注模型平台的NC、SA、商业模型许可，社区照片不得自动复制进营销材料。  
## 07 原始证据与资源索引  
检索与访问日期：2026-11-06。以下均为作者、项目组织或官方课程的可点击原始链接；标为“报道”的用于确认报道时间而非证明项目首次发布。  
[micro:bit 触摸吉他](https://www.microbit.org/projects/make-it-code-it/guitar-1-touch-tunes/)  micro:bit 官方触摸吉他课程（教程/程序/许可）  

[micro:bit 音程升级](https://www.microbit.org/projects/make-it-code-it/guitar-3-octaves/)  micro:bit 音程/八度升级课程  

[Scratch 吉他](https://www.microbit.org/projects/make-it-code-it/scratch-guitar/)  micro:bit Scratch 吉他版  

[Nestbolt 源码](https://github.com/skulitom/Nestbolt)  Nestbolt 源码与技术/测试说明  

[Nestbolt 演示](https://skulitom.github.io/Nestbolt/)  Nestbolt 浏览器演示  

[Nestbolt 依赖声明](https://github.com/skulitom/Nestbolt/blob/main/THIRD_PARTY_NOTICES)  Nestbolt 第三方依赖许可  

[ESP32 Fluid 源码](https://github.com/Vateva/Esp32FluidSimulation8x8)  ESP32流体模拟 GitHub（BOM、引脚、项目说明）  

[ESP32 Fluid 外壳](https://github.com/Vateva/Esp32FluidSimulation8x8/tree/main/Casing%20and%20box)  ESP32 Fluid: 机壳设计目录  

[ESP32 Fluid 手册](https://github.com/Vateva/Esp32FluidSimulation8x8/blob/main/8x8FluidSimulationUserManual.pdf)  ESP32 Fluid: 用户手册PDF  

[Suutari20 源码](https://github.com/Squalius-cephalus/suutari20)  Suutari20 原仓库（KiCad/Gerber/固件/许可）  

[Suutari20 装配](https://github.com/Squalius-cephalus/suutari20/wiki/Getting-started)  Suutari20 原作者Build Guide导航  

[Suutari20 报道](https://www.open-electronics.org/suutari20-a-modular-macro-keyboard-built-on-3-5-mm-audio-jacks/)  Suutari20 2026-10-31报道（日期归类）  

[XGO Duck 硬件](https://github.com/LuwuDynamics/xgoduck_hardware)  XGO Duck 硬件/结构/BOM/装配  

[XGO Duck 许可](https://github.com/LuwuDynamics/xgoduck_hardware/blob/master/LICENSING.md)  XGO Duck 明确的许可状态文件  

[XGO Duck 程序](https://github.com/LuwuDynamics/xgoduck_runtime_arduino)  XGO Duck Arduino运行仓库  

[XGO Duck 报道](https://www.open-electronics.org/xgo-duck-the-open-source-robot-duck-that-walks-with-neural-policies/)  XGO Duck 2026-11-01报道  

[IronEar 源码](https://github.com/PionEars/IronEar)  IronEar 团队GitHub与分阶段公开清单  

[IronEar 官方](https://www.crowdsupply.com/ironear-technologies/ironear)  IronEar 官方众筹/许可说明  

[IronEar 报道](https://www.open-electronics.org/ironear-the-privacy-first-audio-sensor-that-recognises-500-sounds-on-device/)  IronEar 2026-11-03报道  

完 / AHA MAKER RESEARCH 008  
核查日 2026-11-06    ·