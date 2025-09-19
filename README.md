

-----

# 🚀 RISC-V Reference SoC Tapeout Program

### Week 0: The Genesis - Environment Setup

> Welcome, architect\! This repository documents the journey of building a full System-on-Chip (SoC) from the ground up using open-source EDA tools. This is my logbook for the tasks, learnings, and milestones achieved throughout this program.
>
> **\#RISCV \#SoC \#VSD \#KunalGhosh \#Tapeout**

-----

## 🛠️ Task 2: Toolchain Installation

This section covers the setup of our digital design workshop. The goal is to install all the necessary open-source tools required for synthesis, simulation, and verification.

### System Blueprint (Prerequisites)

Before we begin, ensure your machine (or virtual machine) meets these specifications:

  * 🧠 **RAM:** 6GB+
  * 💾 **HDD:** 50GB+ of free space
  * 🖥️ **OS:** Ubuntu 20.04 or later
  * ⚙️ **CPU:** 4 virtual CPUs (vCPUs) allocated

-----

### The Toolkit (Installation Steps)

First, let's update our system's package list.

```bash
sudo apt-get update
```

Now, we'll install each tool one by one.

#### 1\. Yosys (Synthesis)

Yosys will be our workhorse for converting Verilog RTL designs into a gate-level netlist.

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
```

#### 2\. Icarus Verilog (Simulation)

Icarus Verilog, or `iverilog`, is a Verilog compiler and simulator that we'll use to test our designs.

```bash
sudo apt-get install iverilog
```

#### 3\. GTKWave (Waveform Viewer)

To visualize the results of our simulations, we need a waveform viewer. GTKWave is a popular and powerful choice.

```bash
sudo apt-get install gtkwave
```

-----

### ✅ Verification: Tool Snapshot

Below is a snapshot of my terminal confirming the successful installation and version check of all the required tools.

*(You can add your screenshot here by editing this README file and dragging the image in or using a markdown link)*

-----

## 🖥️ OS Philosophy: Virtual Machine vs. Dual Boot

Choosing how to run Ubuntu is a key first step. Here’s a quick breakdown of the two common approaches.

  * **Virtual Machine (The Sandbox)** 샌드박스

      * **What it is:** Running Ubuntu as an application inside your primary OS (like Windows or macOS) using software like VirtualBox or VMWare.
      * **Pros:** It's completely isolated, so there's no risk to your main system. It's easy to delete and start over if something goes wrong.
      * **Cons:** There's a slight performance overhead since you're running two operating systems simultaneously.
      * **Verdict:** **Highly recommended** for this program. It's safe, clean, and perfectly adequate for the tasks ahead.

  * **Dual Boot (The Split-Personality)** 듀얼 부팅

      * **What it is:** Installing Ubuntu alongside your primary OS on a separate partition of your hard drive. When you start your computer, you choose which OS to load.
      * **Pros:** You get the full, native performance of your hardware as Ubuntu has direct access to all resources.
      * **Cons:** The setup is more complex and carries a small risk of messing up your bootloader or partitions.
      * **Verdict:** A great option for power users who want maximum performance, but not necessary for this program.

-----

## 🙏 Acknowledgements

A huge thanks to **Kunal Ghosh** and the entire **VSD (VLSI System Design)** team for creating this invaluable learning opportunity and guiding us through the intricate world of SoC design and tapeout.
