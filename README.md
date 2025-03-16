# 一、小组信息及分工  

  姓名  | 学号  | 联系方式  |  负责方向  |  技术栈  
  ---- |----- |------ |------- |-------- 
  韩承育 | 2405024131 | 13504698855 | 软件+视觉 | esp32、stm32
  张思怡 | 2405034402 | 13633566953 | 硬件+视觉 | 画板、简单的编程和建模
  郑丹儿 | 2405034412 | 13380409656 | 软件+视觉 | esp32、stm32
# 二、方向选择
## 1、选题及分析
（1）选题：送药小车  
（2）分析：当前安排契合智能控制与小车技术方向。硬件搭建由成员 A 负责，为小车构建基础物理框架；成员 B 主导 STM32 代码编写，实现运动控制等核心功能；成员 C 兼顾辅助与视觉学习，提升小车感知能力。多方面协同发展，有望打造出智能、高效、稳定的送药小车。
## 2、所需技术栈
stm单片机，电机驱动，传感器（摄像头），陀螺仪，无线通信，OLED显示屏，LED指示灯，图像识别算法（阈值巡线算法，数字识别算法），控制算法（PID）
# 三、设备清单
1、工具：螺丝刀、胶水、电烙铁、各种型号的螺丝、剪刀等  
2、硬件材料：主控stm32F103c8t6、电机驱动TB6612、摄像头k230、陀螺仪MPU6050、灰度传感器、无线通信模块、OLED显示屏、LED指示灯等  
3、软件工具链：图像识别算法、控制算法、程序设计
# 四、学习计划
1、3月16日 - 3月22日 ：  
（1）成员A（硬件）：深入研究小车硬件电路设计，绘制详细的电路图，重点规划各硬件模块，如STM32单片机最小系统、电机驱动模块（TB6612）、k230摄像头模块、陀螺仪模块、灰度传感器模块、无线通信模块（UART + 蓝牙）、OLED显示屏模块和LED指示灯模块的连接方式。开始准备硬件所需的电子元器件采购清单，对比不同供应商的产品质量和价格，确保元器件的性能符合项目要求。  
（2）成员B（软件 - 视觉与MSP系列学习）：搭建k230开发环境，学习k230的基本操作，包括摄像头参数设置、图像采集与保存。阅读k230官方文档，了解其内置的视觉算法库，如颜色识别、形状识别等基础算法原理。初步学习2021电赛F题国一方案中视觉相关部分的代码结构，重点分析巡线实现的代码逻辑，尝试理解代码中如何处理图像数据以获取巡线所需的信息。  
（3）成员C（软件 - STM代码）：梳理STM32单片机在送药小车项目中的功能需求，确定需要使用的外设资源，如定时器、串口、GPIO口等。搭建STM32开发环境，熟悉开发工具的使用，包括代码编译、下载和调试。开始编写STM32的基础代码框架，初始化各个外设，为后续连接硬件模块和实现控制功能做准备。   
2、3月23日 - 3月29日:  
（1）成员A（硬件）：根据设计好的电路图，进行PCB版图设计，合理布局各个硬件模块，考虑信号干扰、电源分配等因素，确保电路板的稳定性和可靠性。将设计好的PCB文件发送给制板厂家进行制作，跟踪制板进度，及时处理可能出现的问题。同时，开始对已采购的电子元器件进行焊接前的准备工作，如检查元器件的型号和参数是否正确，清理焊接引脚等。  
（2）成员B（软件 - 视觉与MSP系列学习）：深入学习k230的图像识别算法，特别是阈值巡线算法和数字识别算法。通过实际操作k230，采集不同场景下的图像数据，运用所学算法进行处理，不断优化算法参数，提高识别的准确性和稳定性。开始学习MSP系列板子的基础知识，包括芯片架构、寄存器配置等内容，搭建MSP系列开发环境，为后续学习代码开发做准备。  
（3）成员C（软件 - STM代码）：编写STM32与电机驱动模块的通信代码，实现通过STM32控制电机的正反转和转速调节。编写STM32与k230的串口通信代码框架，确保两者之间能够稳定地传输数据，如接收k230发送的巡线误差和数字识别结果等信息。对已编写的代码进行初步调试，检查是否存在语法错误和逻辑错误，及时进行修正。  
3、3月30日 - 4月5日   
（1）成员A（硬件）：完成电路板的焊接工作，仔细检查焊接质量，确保每个元器件焊接牢固，无虚焊、短路等问题。对焊接好的电路板进行初步的硬件测试，如检查电源是否正常供电，各个模块是否能够正常初始化等。使用示波器、万用表等工具，检测硬件模块的信号输出是否符合预期，及时排查和解决硬件故障。   
（2）成员B（软件 - 视觉与MSP系列学习）：在k230上实现完整的巡线功能，结合阈值巡线算法，使小车能够准确地沿着预设的红线行驶。开始学习MSP系列板子的代码开发，参考相关技术文档和开源项目，编写一些简单的测试程序，如控制LED灯闪烁、读取按键状态等，熟悉MSP系列芯片的代码编写方法。   
（3）成员C（软件 - STM代码）：编写STM32与陀螺仪模块的通信代码，获取小车的角度信息，为后续的转向控制提供数据支持。结合电机控制代码和陀螺仪数据，实现基于PID控制算法的小车转向控制，通过调整PID参数，优化小车的转向性能，使小车能够稳定地行驶在预设路径上。对已实现的功能进行集成测试，检查各模块之间的协同工作情况，及时发现和解决问题。  
4、4月6日 - 4月11日  
（1）成员A（硬件）：对硬件系统进行全面的优化和调试，进一步检查硬件的稳定性和可靠性。对各个硬件模块进行压力测试，如长时间运行电机、频繁进行数据传输等，观察硬件是否出现异常情况，及时进行改进。配合软件团队进行硬件与软件的联合调试，确保硬件与软件之间的接口正常，数据传输准确无误。  
（2）成员B（软件 - 视觉与MSP系列学习）：在OpenMV上实现数字识别功能，通过训练模型和优化算法，提高数字识别的准确率。将MSP系列板子的学习成果与送药小车项目相结合，探索MSP系列板子在项目中的应用场景，如辅助控制、数据处理等。与成员C协作，将OpenMV和MSP系列的相关代码与STM32代码进行集成，实现整体功能的初步整合。  
（3）成员C（软件 - STM代码）：完善STM32代码的功能，实现与其他硬件模块的全面通信和协同工作，如与超声测距模块、灰度传感器模块、无线通信模块等的通信。对整个软件系统进行优化，提高代码的运行效率和稳定性，减少资源占用。配合成员B进行软件功能的测试和优化，确保送药小车能够按照预期的功能运行，如准确巡线、识别数字、寻找药房等。    
5、4月11日 - 5月9日 ：  
若题目一基本完成，着手制定通用方案的计划并完美实现题目  
若题目一未完成，则继续完善。在此期间，负责写代码的两人学习MSP系列板子的代码开发，硬件方向的一人学习3D打印机操作并完成技术报告。在学习MSP系列板子代码时，参考相关技术文档和开源项目，了解MSP系列芯片的架构、功能特性，掌握其开发环境搭建和代码编写方法，为后续在项目中应用MSP系列板子做好准备。   
6、5月12日 - 6月6日：  
继续推进通用方案的完成，内容包括红外循迹、陀螺仪应用、电机控制、舵机控制、LED指示灯设计、双车通信等方面的实现。结合之前学习的k230和MSP系列板子的知识，将其应用到通用方案中，优化项目的功能和性能。   
7、放假 - 设备清单公布：  
持续完善通用方案，密切关注设备清单公布。在设备清单公布后，通过网络查找相关题目，并借鉴他人的开源代码，进一步丰富项目思路和技术实现手段。  
# 五、其他重要事项  
1. 代码风格统一：  
借助题目一的开发过程，沟通协调两人的代码风格，提高代码的可读性和可维护性，确保团队开发的代码具有一致性。   
2. 赛事准备：  
完成上述各项任务后，全力准备开赛，确保项目在比赛中能够稳定运行，充分展示项目的功能和优势。

