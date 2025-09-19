
## 🛠️ Task 0: Toolchain Installation

This section covers the setup of our digital design workshop. The goal is to install all the necessary open-source tools required for synthesis, simulation, and verification.

-----

### The Toolkit (Installation Steps)

First, let's update our system's package list.

```bash
sudo apt-get update
```

Now, we'll install each tool one by one.

#### 1\. Yosys (Synthesis)

Yosys will be our workhorse for converting Verilog RTL designs into a gate-level netlist.

**make sure to run these commands one by one**

```bash
# Install dependencies required to build Yosys from source
sudo apt-get install build-essential clang bison flex \
libreadline-dev gawk tcl-dev libffi-dev git \
graphviz xdot pkg-config python3 libboost-system-dev \
libboost-python-dev libboost-filesystem-dev zlib1g-dev

# Clone the Yosys repository
git clone https://github.com/YosysHQ/yosys.git

# Navigate into the directory and build
cd yosys
make config-gcc
make
sudo make install

#if you get an error like shown in image do the same as done in the image

```
![image alt](https://github.com/BAMB00SEVEN/Know_Z3R0/blob/main/Screenshot%20from%202025-09-19%2018-39-37.png?raw=true)

>The final screen after successful installation
><img width="1633" height="1133" alt="Image" src="https://github.com/user-attachments/assets/e4fe1430-fbc8-49db-a8f7-afb787708068" />

#### 2\. Icarus Verilog (Simulation)

Icarus Verilog, or `iverilog`, is a Verilog compiler and simulator that we'll use to test our designs.

```bash
sudo apt-get update
sudo apt-get install iverilog
```

#### 3\. GTKWave (Waveform Viewer)

To visualize the results of our simulations, we need a waveform viewer. GTKWave is a popular and powerful choice.

```bash
sudo apt-get update
sudo apt-get install gtkwave
```

-----

### ✅ Verification: Tool Snapshot

Below is a snapshot of my terminal confirming the successful installation and version check of all the required tools.

*(You can add your screenshot here by editing this README file and dragging the image in or using a markdown link)*

-----
