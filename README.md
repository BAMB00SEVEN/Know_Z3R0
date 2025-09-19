

-----

# 🚀 RISC-V Reference SoC Tapeout Program

### Week 0: The Genesis - Environment Setup

> Welcome, architect\! This repository documents the journey of building a full System-on-Chip (SoC) from the ground up using open-source EDA tools. This is my logbook for the tasks, learnings, and milestones achieved throughout this program.
>
> 

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
