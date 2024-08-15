# Side-Protocol-Node-Guide

Sure! Here’s a rephrased version of the guide:

---

# 🛠 Node Installation & Configuration Guide

This guide will walk you through installing and configuring the **sided** binary for your node.

---

## 💻 Hardware Requirements

### Minimum Specs:

- **CPU**: 4 cores  
- **RAM**: 8 GB  
- **Storage**: 500 GB  
- **Network**: 1 Gbps

---

## 🖥 Operating System

The OS choice is entirely up to you! You can compile the **sided** daemon on most modern Linux distributions as well as newer versions of macOS. 

*Note: This guide uses Ubuntu LTS as an example. If you’re using a different OS, make sure to modify the commands to suit your environment.*

---

## ⚙️ Prerequisites

Before starting, ensure you have **Golang v1.22.0** installed. You can find the necessary downloads and instructions on the [official Go website](https://go.dev/dl/).

---

## 🔨 Building the **sided** Binary

### 1. Verify Your Go Installation

Ensure you have the required version of Go installed by running:

```bash
go version
```

The version should match **v1.22.0** as mentioned in the prerequisites.

### 2. Clone the Repository

First, remove any existing **side** directories you may have cloned earlier, then re-clone the latest repository:

```bash
git clone https://github.com/sideprotocol/side.git
cd side
git checkout v0.9.0
```

### 3. Compile the Binary

Use the following command to compile the **sided** binary:

```bash
make install
```

The binary will be stored in your `$GOBIN` directory. If this directory is already in your `$PATH`, you’ll be able to run the **sided** binary directly.

### 4. Update Your PATH (If Needed)

If the **sided** binary isn't accessible, ensure the following lines are added to your `.bashrc`, `.zshrc`, or terminal profile to include `$GOBIN` in your `$PATH`:

```bash
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
```

### 5. Verify Installation

Finally, verify the installation by checking the **sided** version:

```bash
sided version
```

You should see `0.9.0` as the output.

---

If you run into any issues with the PATH setup, be sure to review the [Go installation documentation](https://go.dev/dl/) for additional guidance.

---

Now, you're all set! 🎉
