# EST1602 电子技术与系统实验
该课程是上海交通大学2024级电院ai新开设课程，配合EST1601《电子技术与系统》，由集成电路学院张宸老师授课，耿琛博和周卓珊任助教。
课程内容由两条主线交织，一个是pytorch的使用和模型的稀疏，另一个是在线上平台做电路仿真。共六个实验：
- pytorch的基本使用
- 电路平台的使用 基尔霍夫定律的验证、基本放大电路的搭建
- 搭建与非门、半加器、全加器、乘法器
- 模型的剪枝
- 搭建一个矩阵乘法的脉动阵列
- 模型的量化

本项目为本人的大作业报告和源代码文件，其中电路文件请使用https://www.falstad.com/circuit/circuitjs.html 打开。
- 电路部分实验从三极管放大电路开始，搭建异或门电路，进而实现和验证了1bit半加器、1bit全加器、4bit乘法
器、8bit加法器。再结合D-触发器、数据选择器等组合逻辑，搭建了一个含重置和保持两个控制功能的2\*2、
4bit矩阵乘法器，并成功通过验证。本实验还实现并验证了一个基于内积的2\*2、4bit矩阵乘法器。
- 稀疏部分实验以数值大小的逐元素稀疏剪枝。以绝对值为分数标准，根据期望的稀疏度找到分数的阈值，删除小于该
分数的权重，得到稀疏张量。 本实验为不同层设置不同的稀疏度，并对剪枝过后的模型微调，再训练5轮，得
到一个理想的稀疏模型。


This course is a newly introduced offering for the 2024 cohort of AI majors in SEIEE, SJTU. It complements **EST1601 "Electronic Technology and Systems,"** and is taught by **Zhang Chen**, with **Geng Chenbo** and **Zhou Zhuoshan** serving as TAs.

The course content intertwines two main threads:
1.  The use of **PyTorch** and **model sparsification**.
2.  **Circuit simulations** on an online platform.

## Experiment List
The course consists of six experiments:

1.  Basic usage of PyTorch
2.  Introduction to the circuit platform: verification of Kirchhoff's laws and construction of basic amplifier circuits
3.  Building NAND gates, half adders, full adders, and multipliers
4.  Model pruning
5.  Constructing a systolic array for matrix multiplication
6.  Model quantization

## Project Description
This project comprises my final assignment report and source code files.
*   **Circuit files** can be opened using [Falstad's CircuitJS](https://www.falstad.com/circuit/circuitjs.html).

## Circuit Experiments
The circuit experiments involved the following implementations and verifications:
*   Began with a **transistor amplifier circuit**.
*   Constructed an **XOR gate**.
*   Implemented and verified a **1-bit half adder**, a **1-bit full adder**, a **4-bit multiplier**, and an **8-bit adder**.
*   Integrated **D flip-flops**, **multiplexers**, and other combinational logic components to build a **2x2, 4-bit matrix multiplier** with **reset and hold control functions**.
*   Additionally, implemented and verified a **2x2, 4-bit matrix multiplier** based on **inner product operations**.

## Sparsity Experiments
The sparsity experiments involved:
*   **Element-wise pruning** based on weight magnitude.
*   Using **absolute values** as the scoring criterion to determine a pruning threshold according to a desired sparsity level.
*   Weights scoring below this threshold were pruned, resulting in a **sparse tensor**.
*   **Different sparsity levels** were set for various layers.
*   The pruned model was **fine-tuned** and **retrained for 5 epochs**, ultimately yielding an optimally sparse model.
