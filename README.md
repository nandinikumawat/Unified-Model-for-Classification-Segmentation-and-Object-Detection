# Object Detection, Segmentation and Classification on FPGA (LeNet-5 and BNN)

## Overview
This project aims to implement Convolutional Neural Networks (CNNs) for object detection and classification on the PYNQ Z2 FPGA board. Specifically, it utilizes LeNet-5 for handwritten and machine-printed character detection and Binary Neural Networks (BNNs) for object detection.

## Project Structure
The project is structured as follows:
- `vitis-hls/`: Contains Vitis HLS project files.
- `vivado/`: Contains Vivado project files.
- `jupyter-notebooks/`: Jupyter notebooks for interfacing with the FPGA.
- `python-scripts/`: Python scripts for data processing and analysis.

## Vitis HLS Flow
### 1. Design Entry
In the `vitis-hls/` directory, you can find the high-level language design (C or C++) for LeNet-5 and BNN.

### 2. Verification
Use the provided testbenches in `vitis-hls/verification/` to ensure the correctness of the design.

### 3. High-Level Synthesis
Run Vitis HLS on the high-level code to convert it into Register Transfer Level (RTL) implementation.

### 4. Optimization
Vitis HLS performs optimizations, including pipelining, loop unrolling, and memory partitioning, to enhance performance.

### 5. Verification
Verify the optimized RTL code to ensure it meets design requirements.

### 6. Export
Export the RTL code and constraints to the Vivado tool for synthesis and implementation.

## Vivado Flow
### 1. Design Entry
Navigate to `vivado/` to find Vivado project files. Create or import design files, specify top-level modules, and set parameters.

### 2. Block Design
Open the IP catalog to add necessary IP, processing system, and other pre-defined modules.

### 3. Run Automation
Run Vivado automation for design convenience.

### 4. Validation
Validate the block design, check addresses using the address editor, and create an HDL wrapper for a single module.

### 5. Synthesis
Synthesize the design to generate a netlist that describes the behavior of the design in terms of logic gates and flip-flops.

### 6. Simulation
Simulate the design using a testbench to verify functionality before implementation.

### 7. Design Analysis
Analyze the design for timing violations, resource usage, and power consumption.

### 8. Implementation
Map the design to the target FPGA, generate routing and placement information.

### 9. Bitstream Generation
Generate a bitstream file containing the configuration information for the target FPGA device.

### 10. Hardware Validation
Load the bitstream onto the target device, test the design to ensure correct behavior, and measure performance.

## Methodology
### LeNet-5 Implementation
- Developed LeNet IP using Vitis HLS.
- Integrated with Zynq processing system in Vivado.
- Used 32-bit General Purpose and High-Performance Axis Slave interfaces.

### BNN for Object Detection
- Utilized Binary Neural Networks for efficient object detection.
- Trained and deployed BNN on the PYNQ board.

## Results
### LeNet-5 Output
- Presented power consumption data.
- Output accuracy and time taken for 32-bit General Purpose and High-Performance Axis Slave interfaces.

### BNN Model Output
- Object detection and classification results.
- Displayed images with identified objects.

## Conclusion and Future Scope
### Conclusion
- Successfully implemented CNN and BNN on FPGA.
- Improved efficiency and accuracy of object detection.

### Future Scope
- Further optimization using pruning and quantization.
- Explore real-time applications and deployment in resource-constrained devices.

## How to Use
- Instructions on setting up the environment and running the project.

## License
- Specify the license under which the project is distributed.

## Contributors
- List of contributors and how to contribute.

