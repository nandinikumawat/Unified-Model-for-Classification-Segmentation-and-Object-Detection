# FPGA Object Detection, Classification, and Segmentation

## Introduction
This repository presents the implementation of object detection, classification, and segmentation on an FPGA board, specifically the PYNQ Z2 board. The project explores various existing architectures for these tasks and demonstrates the implementation of LeNet-5 for handwritten and machine-printed character detection using Jupyter Notebook and Python programming language.

![LeNet IP Developed in Vitis HLS](/docs/images/lenet_ip.png)

## Project Structure
- **/src**: Source code for FPGA implementation
- **/docs**: Documentation and project-related documents
- **/results**: Outcome and output files
- **/notebooks**: Jupyter notebooks for development
- **/scripts**: Helper scripts for automation

## LeNet-5 Implementation
The LeNet-5 architecture is developed in Xilinx Vitis HLS and integrated with the Zynq processing system using Xilinx Vivado. The block design involves the use of both general-purpose axis slave interfaces and high-performance axis slave interfaces.

![32-bit General Purpose AXI Slave Interface](/docs/images/general_purpose_axi.png)
![LeNet's Zynq Block Design (using General Purpose Axis Slave)](/docs/images/lenet_zynq_block_design.png)

The communication between the Zynq PS side and LeNet IP core is explained, utilizing m_axi protocol (AXI Master) and s_axilite protocol for small data transmission. After design validation, the HDL wrapper is created, and synthesis and simulation are performed before mapping to the target FPGA device.

## BNN-Based Object Detection
In addition to LeNet-5, the project implements object detection using Binary Neural Networks (BNN). The BNN architecture is characterized by binarized weights and activations, leading to reduced memory and computation requirements, making it efficient for resource-constrained environments.

The BNN implementation involves the instantiation of a custom driver class, the use of overlays in PYNQ for hardware design loading, and the deployment of the trained BNN model on the FPGA.

## Results
### LeNet-5 Output
#### 32-bit General Purpose AXI Slave Interface
Accuracy: 95%
Total Time: 50 ms

#### 32-bit High-Performance AXI Slave Interface
Accuracy: 92%
Total Time: 30 ms

### BNN Model Output
The BNN model demonstrates efficient object detection and classification, showcasing reduced memory and computation requirements.

![BNN Model Output](/docs/images/bnn_output.png)

## Conclusion and Future Scope
In conclusion, this project successfully implements LeNet-5 and BNN for object detection, classification, and segmentation on an FPGA board. The use of Jupyter Notebook for hardware interfacing and Python programming language enhances the accessibility and flexibility of the implementation.

### Future Scope
The BNN-based object detection approach shows promise for real-time and efficient systems in resource-constrained environments. Ongoing research aims to address challenges in training and optimization, paving the way for further improvements in performance.

For detailed instructions, setup, and additional information, refer to the documentation in the `/docs` folder.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.



