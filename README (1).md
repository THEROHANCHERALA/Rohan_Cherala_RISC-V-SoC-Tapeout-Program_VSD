# Digital Design Toolchain Setup

This repository documents the installation of essential open-source tools for digital design and verification:
- **Yosys** – RTL synthesis
- **Icarus Verilog (iverilog)** – Verilog simulation
- **GTKWave** – waveform visualization

---

## 📦 Dependencies

Install required packages:

```bash
sudo apt-get update
sudo apt-get install gperf build-essential clang lld bison flex libfl-dev graphviz xdot pkg-config python3 libboost-system-dev libboost-python-dev libboost-filesystem-dev zlib1g-dev git
```

> 💡 If `libboost-python-dev` is not available, install all Boost libraries:
> ```bash
> sudo apt-get install libboost-all-dev
> ```

---

## 🔧 Install Yosys

```bash
git clone https://github.com/YosysHQ/yosys.git
cd yosys
make config-gcc
git submodule update --init --recursive
make
sudo make install
```

![Yosys Installed](Images/yosys_installation_done.jpeg)

---

## 🖥️ Install Icarus Verilog

```bash
sudo apt-get update
sudo apt-get install iverilog
```

![Iverilog Status](Images/iverilog_status.png)

---

## 📊 Install GTKWave

```bash
sudo apt-get update
sudo apt-get install gtkwave
```

---

## ✅ Verification

- Run `yosys -V` → should print version info.
- Run `iverilog -V` → should print version info.
- Run `gtkwave` → GUI should open.

---

## 📂 Folder Structure

```
project/
│── README.md
│── Images/
│    ├── yosys_installation_done.jpeg
│    └── iverilog_status.png
```

---

## 🙌 Credits
- [YosysHQ](https://yosyshq.net/yosys/)
- [Icarus Verilog](http://iverilog.icarus.com/)
- [GTKWave](http://gtkwave.sourceforge.net/)
