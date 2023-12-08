+# FPGA Object Detection, Classification, and Segmentation

## Introduction
This repository presents the implementation of object detection, classification, and segmentation on an FPGA board, specifically the PYNQ Z2 board. The project explores various existing architectures for these tasks and demonstrates the implementation of LeNet-5 for handwritten and machine-printed character detection using Jupyter Notebook and Python programming language.

![image](https://github.com/nandinikumawat/Unified-Model-for-Classification-Segmentation-and-Object-Detection/assets/63352345/a167c3b4-5aef-4846-b2ab-a80216d04a39)


## Project Structure
- **/src**: Source code for FPGA implementation
- **/docs**: Documentation and project-related documents
- **/results**: Outcome and output files
- **/notebooks**: Jupyter notebooks for development
- **/scripts**: Helper scripts for automation

## LeNet-5 Implementation
The LeNet-5 architecture is developed in Xilinx Vitis HLS and integrated with the Zynq processing system using Xilinx Vivado. The block design involves the use of both general-purpose axis slave interfaces and high-performance axis slave interfaces.

![image](https://github.com/nandinikumawat/Unified-Model-for-Classification-Segmentation-and-Object-Detection/assets/63352345/21474d6f-b640-4c31-b176-d8f71f0b23da)

![image](https://github.com/nandinikumawat/Unified-Model-for-Classification-Segmentation-and-Object-Detection/assets/63352345/010b1d23-ae57-43c7-8e24-25b127c9cae8)

The communication between the Zynq PS side and LeNet IP core is explained, utilizing m_axi protocol (AXI Master) and s_axilite protocol for small data transmission. After design validation, the HDL wrapper is created, and synthesis and simulation are performed before mapping to the target FPGA device.

## BNN-Based Object Detection
In addition to LeNet-5, the project implements object detection using Binary Neural Networks (BNN). The BNN architecture is characterized by binarized weights and activations, leading to reduced memory and computation requirements, making it efficient for resource-constrained environments.

The BNN implementation involves the instantiation of a custom driver class, the use of overlays in PYNQ for hardware design loading, and the deployment of the trained BNN model on the FPGA.

## Results

![image](https://github.com/nandinikumawat/Unified-Model-for-Classification-Segmentation-and-Object-Detection/assets/63352345/afc3cab7-f4bd-4a37-b588-c18c901b7365)

![image](https://github.com/nandinikumawat/Unified-Model-for-Classification-Segmentation-and-Object-Detection/assets/63352345/448bb32e-a9c1-4398-8730-ea2308e6e25e)

### LeNet-5 Output
#### 32-bit General Purpose AXI Slave Interface

![image](https://github.com/nandinikumawat/Unified-Model-for-Classification-Segmentation-and-Object-Detection/assets/63352345/3c763a2f-b728-4b89-b28c-89014c280589)

#### 32-bit High-Performance AXI Slave Interface

![image](https://github.com/nandinikumawat/Unified-Model-for-Classification-Segmentation-and-Object-Detection/assets/63352345/6b1d679e-ce32-403e-b20c-52ebb337798a)

### BNN Model Output
The BNN model demonstrates efficient object detection and classification, showcasing reduced memory and computation requirements.

![image](https://github.com/nandinikumawat/Unified-Model-for-Classification-Segmentation-and-Object-Detection/assets/63352345/c0823055-7196-4d91-8697-ff07469aaf5c)

## Conclusion and Future Scope
In conclusion, this project successfully implements LeNet-5 and BNN for object detection, classification, and segmentation on an FPGA board. The use of Jupyter Notebook for hardware interfacing and Python programming language enhances the accessibility and flexibility of the implementation.

### Future Scope
The BNN-based object detection approach shows promise for real-time and efficient systems in resource-constrained environments. Ongoing research aims to address challenges in training and optimization, paving the way for further improvements in performance.




