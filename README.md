# Image Processing on a Zynq FPGA Board

Project Overview

This project implements image processing on an FPGA, with a focus on applying a Box Blur filter using a 3x3 kernel. The implementation includes the development of custom hardware modules, testing and simulation, and generating the final output image using Vitis SDK. The Box Blur technique is a simple yet effective method of smoothing an image by averaging the pixel values within a 3x3 neighborhood.

Key Project Stages

1. Module Development

The image processing pipeline is divided into three main hardware modules:

Line Buffer Module: This module is crucial for managing intermediate pixel data during image processing. It stores multiple lines of pixel values to ensure efficient data flow through the convolution process.

Convolution Module: Performs the convolution operation using the 3x3 Box Blur kernel. This module reads pixel data from the line buffer and computes the average of the pixel values in the 3x3 region, applying the blur filter.

Control Logic: The control logic coordinates the operation of the line buffer and convolution modules, ensuring smooth data flow and proper timing.

2. Integration and IP Packaging
   
The three modules (Line Buffer, Convolution, and Control Logic) are integrated into a cohesive IP (Intellectual Property) package. This package can be reused or modified for other image processing tasks.

4. Testing and Simulation
   
A comprehensive testbench is created to simulate the integrated IP package. The testbench verifies the functionality and correctness of the image processing pipeline, ensuring that the Box Blur filter is applied as expected.

6. Vitis SDK Integration
   
The final step is integrating the project into Vitis SDK. Using the SDK, the image processing IP is deployed onto the FPGA. The output image, after the Box Blur filter is applied, is generated and analyzed to ensure proper functionality.
