

-----

# 🚀 RISC-V Reference SoC Tapeout Program

### Week 0: The Genesis - Environment Setup

>Welcome, architects! This repository documents the journey of building a full System-on-Chip (SoC) from the ground up using open-source EDA tools. This is my logbook for the tasks and learnings in this massive program, which brings together over **3500+** participants from around the globe.
> 
>
> 

### System Blueprint (Prerequisites)

Before we begin, ensure your machine (or virtual machine) meets these specifications:

  * 🧠 **RAM:** 6GB+
  * 💾 **HDD:** 50GB+ of free space
  * 🖥️ **OS:** Ubuntu 20.04 or later
  * ⚙️ **CPU:** 4 virtual CPUs (vCPUs) allocated
-----


## 🖥️ OS Philosophy: Virtual Machine vs. Dual Boot

Choosing how to run Ubuntu is a key first step. Here’s a quick breakdown of the two common approaches.

  * **Virtual Machine (The Sandbox)** 

      * **What it is:** Running Ubuntu as an application inside your primary OS (like Windows or macOS) using software like VirtualBox or VMWare.
      * **Pros:** It's completely isolated, so there's no risk to your main system. It's easy to delete and start over if something goes wrong.
      * **Cons:** There's a slight performance overhead since you're running two operating systems simultaneously.
      * **Verdict:** **Highly recommended** for this program. It's safe, clean, and perfectly adequate for the tasks ahead.
      * Here is a detailed youtube video for seamless experience of running ubuntu in a virtual machine ------- https://youtu.be/Hva8lsV2nTk

  * **Dual Boot (The Split-Personality)**

      * **What it is:** Installing Ubuntu alongside your primary OS on a separate partition of your hard drive. When you start your computer, you choose which OS to load.
      * **Pros:** You get the full, native performance of your hardware as Ubuntu has direct access to all resources.
      * **Cons:** The setup is more complex and carries a small risk of messing up your bootloader or partitions.
      * **Verdict:** A great option for power users who want maximum performance, but not necessary for this program.
      * **I did it this way as i am confortable with dual boot.**
      * Here is a detailed youtube video for dual boot through windows, for any doubts during installation search the issue on google you will most likely find solution to every issue otherwise you have you best friend AI tools to get your troubleshooting done
------ https://youtu.be/alFosqQ1ang

-----

## 🙏 Acknowledgements

This invaluable learning opportunity is made possible by a massive collaborative effort. A huge thanks to the key organizers and partners:

* VSD (VLSI System Design), led by Kunal Ghosh Sir, for creating and spearheading this initiative.

* IIT Gandhinagar for their crucial academic partnership.

* RISC-V International for their support in promoting the open RISC-V standard.

* The global Open Source VLSI Community for building and maintaining the powerful EDA tools that form the backbone of this program.
