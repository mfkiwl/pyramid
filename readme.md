# Image Pyramid Generator

In this paper, we present an image pyramid accelerator for embedded processors that generates image pyramids of up to 24-levels of down-sampled resolutions for the input image. Since image pyramids are crucial for the coarse-to-fine analy-sis of many computer vision problems, more resolution levels in the image pyra-mid can improve the parameter-estimation accuracy. Furthermore, the down-sampling filters used in the proposed design is based on a long-tap Sine-windowed Sinc function filter. Therefore, it preserves more image details than other low-complexity filters such as the bilinear or the bicubic interpolation filter. The proposed circuit is verified on an FPGA development board with a Xilinx Kintex-7 device.

# Specification
The circuit is implemented as a AXI4 master IP. Verilog and Xilinx Vivado 2018.2 are used to develop the logic. The Xilinx KC-705 development board was used as the verification platform.

In the provided workspace, a Microbalze processor is used to run the image pyramid generating software to control the image down-scaling accelerator. The sample system reads an 640x480 input image through the UART port and prints the output image to the UART port. You can enable the loggin function of your terminal emulator (Teraterm Pro in our case) to save the output image(s) to a file. An offline tool can be used to convert the logged images to PGM images for verification.

# Contact Info
Embedded Intelligent Systems Lab (EISL)
Department of Computer Science
National Chiao Tung University
