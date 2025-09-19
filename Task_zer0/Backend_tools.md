

-----

# 🏗️ Back-End & Physical Design Toolkit

Welcome to the physical design stage\! This guide covers the installation of our primary back-end tools: **ngspice** for detailed circuit simulation and **magic** for creating the physical chip layout. Let's get our digital canvas and microscope ready.

-----

## ⚡ ngspice: The Circuit Simulator

**`ngspice`** is an open-source, mixed-signal circuit simulator. Think of it as your virtual electronics workbench. It allows you to analyze the analog behavior of your digital circuits, verifying voltage levels, timing, and power consumption before you ever create a physical device.

### 🔧 Installation from Source

We will compile `ngspice` from its source code to get the latest version.

#### Step 1: 📦 Download & Unpack the Source

First, grab the source code package (the `.tar.gz` file) from the official repository.

> You can find the latest version here: **[ngspice on SourceForge](https://sourceforge.net/projects/ngspice/files/)**
>
> After downloading, unpack the archive. The `tar` command extracts all the files into a new folder.

```bash
# Replace 'ngspice-37' with the version you downloaded
tar -zxvf ngspice-37.tar.gz
```

#### Step 2: 📂 Navigate to the Source Directory

Move into the newly created folder containing the source code.

```bash
cd ngspice-37
```

#### Step 3: 🛠️ Create a Clean Build Directory

It's a best practice to build software in a separate directory to keep the original source code clean.

```bash
mkdir release
cd release
```

#### Step 4: ⚙️ Configure the Build

The `configure` script checks your system for all required dependencies and prepares the custom build files (`Makefiles`).

> The flags we use are important:
>
>   * `--with-x`: Enables a graphical interface.
>   * `--with-readline`: Enables command history and editing in the terminal.
>   * `--disable-debug`: Optimizes the build for performance.

```bash
../configure --with-x --with-readline=yes --disable-debug
```

#### Step 5: 👨‍💻 Compile the Code

Now, we use the `make` command to compile the entire program. This may take a few minutes, so it's a great time to grab a coffee\!

```bash
make
```

#### Step 6: ✅ Install the Program

Finally, install the compiled program onto your system. The `sudo` command is required to grant the necessary permissions to write to system directories.

```bash
sudo make install
```

-----

## 🎨 Magic: The Layout Editor

**Magic** is a legendary VLSI layout editor. It's a "Manhattan-style" editor where all geometry is composed of rectangular shapes. Think of it as a highly advanced digital canvas where you physically draw the different layers (polysilicon, metal, diffusion) that make up the transistors and wires on your chip.

### 🔧 Installation from Source

Magic also works best when built from the latest source code.

#### Step 1: 📦 Install Dependencies

Magic relies on several system libraries for its user interface, scripting capabilities, and graphics. Let's install them all with a single command.

> These packages provide essential components: `tcl/tk` for the scripting and GUI, `X11` for the display server, and `cairo`/`mesa` for graphics rendering.

```bash
sudo apt-get install m4 tcsh csh libx11-dev tcl-dev tk-dev \
libcairo2-dev mesa-common-dev libglu1-mesa-dev libncurses-dev
```

#### Step 2: 📂 Clone the Source Code

We'll download the latest version of Magic directly from its official GitHub repository.

```bash
git clone https://github.com/RTimothyEdwards/magic.git
```

#### Step 3: 🛠️ Navigate and Configure

Move into the cloned `magic` directory and run the configuration script to prepare for the build.

```bash
cd magic
./configure
```

#### Step 4: 👨‍💻 Compile the Code

Just like with ngspice, we use the `make` command to compile the program.

```bash
make
```

#### Step 5: ✅ Install the Program

Use `sudo make install` to copy the compiled files to the correct locations on your system, making the `magic` command available from anywhere in your terminal.

```bash
sudo make install
```

-----

And you're all set\! With **ngspice** and **magic** installed, you now have a powerful suite for analog simulation and physical layout design.
