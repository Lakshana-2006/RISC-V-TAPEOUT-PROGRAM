# RISC-V-TAPEOUT-PROGRAM
# WEEK 0 - Thu, 18 Sep 2025 – Wed, 24 Sep 2025  

## Environment Setup + RTL Simulation Basics  

### Task 1: Initialize GitHub Repository  
- Repository link: [RISC-V-TAPEOUT-PROGRAM](https://github.com/Lakshana-2006/RISC-V-TAPEOUT-PROGRAM)  

---

### Task 2: Install Required Tools  

#### Virtual Machine  
- Download Oracle VirtualBox: [VirtualBox Downloads](https://www.virtualbox.org/wiki/Downloads)  

#### Minimum System Requirements  
- Memory: **6 GB RAM**  
- Disk: **50 GB HDD**  
- OS: **Ubuntu 20.04 or newer**  
- CPU: **4 vCPUs**  

![image](Screenshot1.jpg)

---

### Yosys Installation  
```bash
sudo apt update
git clone https://github.com/YosysHQ/yosys.git
cd yosys

# Install dependencies
sudo apt install make build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 \
    libboost-system-dev libboost-python-dev \
    libboost-filesystem-dev zlib1g-dev -y

# Configure build for GCC
make config-gcc

# Initialize abc submodule
git submodule update --init --recursive

# Compile and install
make
sudo make install
