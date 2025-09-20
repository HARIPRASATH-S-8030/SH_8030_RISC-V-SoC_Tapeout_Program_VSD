# Week 0 : Setting up the Environment for RISC-V tapeout

A brief display of the preliminary works done for booting up the process of RISC-V tapeout programme by VSD - VLSI System Design along with IIT Gandhinagar.

## Tools to be installed

  1.Yosys

  2.iverilog

  3.gtkwave


## Role of each Tools in this tapeout process

 - **Yosys** : Yosys is an open-source RTL synthesis tool widely used in modern chip design flows, especially for RISC-V and other open hardware projects. It converts high-level hardware descriptions written in Verilog into optimized __gate-level netlists__ that map to specific technology libraries. This synthesis step is crucial for bridging the gap between RTL code and physical implementation. Yosys integrates smoothly with open-source place-and-route tools like OpenROAD and supports formal verification workflows to ensure design correctness. Its compatibility with open process design kits (PDKs) such as SkyWater’s 130nm technology enables hobbyists, researchers, and companies to produce tapeout-ready layouts using fully open-source toolchains. Overall, Yosys plays a vital role in accelerating affordable and accessible chip tapeouts by providing a flexible, powerful synthesis solution.

 - **iverilog** : Icarus Verilog, commonly known as iverilog, is a popular open-source Verilog simulation and synthesis tool used primarily for RTL simulation in chip design workflows. Unlike Yosys, which focuses on synthesis, iverilog enables designers to compile and simulate Verilog code to verify functional correctness early in the development cycle. It supports a wide range of Verilog language constructs and is often used to run testbenches that validate RISC-V cores and other digital designs before synthesis. Its lightweight, command-line-driven interface makes it ideal for integration into automated verification pipelines. While not typically used for synthesis or tapeout, iverilog is a fundamental tool for __functional verification__, helping designers catch bugs and ensure proper behavior before moving on to synthesis and physical implementation.

 - **gtkwave** : GTKWave is an open-source waveform viewer widely used in chip design for __visualizing simulation results of digital circuits__. After running RTL simulations with tools like iverilog, designers use GTKWave to inspect signal waveforms and debug the behavior of their hardware designs. It supports multiple waveform file formats (like VCD, LXT) and provides features such as zooming, searching, and hierarchical signal display, making it easier to analyze timing, control signals, and data paths. GTKWave is an essential part of the __functional verification__ process, helping engineers verify that their designs behave as expected before moving to synthesis and tapeout stages. Its lightweight, cross-platform interface makes it a popular choice for both hobbyists and professional chip developers.

## System configuration Required
 - __Memory__ : 6GB RAM, 50 GB HDD 
 - __Operating system__ : Ubuntu 20.04+ 
 - __Virtual CPU__ : 4 vCPU

## Installation commands and verification

 1. **Yosys**
  The following section gives the set of commands to be executed to download the Yosys file, also the snapshots for the downloaded file has also been attached for reference.
  - __Commands__
 ``` bash
 $ sudo apt-get update 
 $ git clone https://github.com/YosysHQ/yosys.git
 $ cd yosys 
 $ sudo apt install make (If make is not installed please install it)  
 $ sudo apt-get install build-essential clang bison flex \libreadline-dev gawk tcl-dev libffi-dev git \graphviz xdot pkg-config python3 libboost-system-dev \libboost-python-dev libboost-filesystem-dev zlib1g-dev 
 $ make config-gcc 
 $ make  
 $ sudo make install 

 ```
 - **Screenshot**
 ![]

2. **iverilog**
The following section gives the set of commands to be executed to download the iverilog file, also the snapshots for the downloaded file has also been attached for reference.
  - __Commands__
 ``` bash
 $ sudo apt-get update 
 $ sudo apt-get install iverilog 

 ```
  - __Screenshot__

3. **gtkwave**
The following section gives the set of commands to be executed to download the gtkwave file, also the snapshots for the downloaded file has also been attached for reference.
  - __Commands__
 ``` bash
 $ sudo apt-get update 
 $ sudo apt install gtkwave

 ```
 - __Screenshot__
 
## Summary
Thus we have installed some of the tools that are required for VLSI - RISC-V Chip design process, making the environment ready.
 


