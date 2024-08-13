# ChasmNetwork_CLI
# How to run Chasm Network with CLI

<img src="https://www.chasm.net/og.png" width="3500"/>


To learn more about Chasm Network, go here. [here](https://network-docs.chasm.net/).



## Step 1: Updates to the system and installation of necessary tools

### Update System Packages
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install cmake pkg-config libssl-dev build-essential -y
```

### Rust and Cargo Installation
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

source $HOME/.cargo/env

## press 1
```

## Step 2: Open a terminal and run the following command to start the Homebrew installation:

### Download and Install Homebrew
```/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
### Wait until the installation finish

If u facing this issue : 
![1](https://raw.githubusercontent.com/mumeido/ChasmNetwork_CLI/main/Issue_1.PNG)

you'll need to create a new user and install Homebrew using that account. Follow these steps:

1. Create a new user and switch to the new user :
   ```bash
     sudo adduser brewuser
     sudo usermod -aG sudo brewuser
     sudo -u brewuser -s
    ```
   ![2](https://raw.githubusercontent.com/mumeido/ChasmNetwork_CLI/main/Issue_2.PNG)
2. Run the installation script:
   ```bash
   bash -c '/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"'
   ```
   ![3](https://raw.githubusercontent.com/mumeido/ChasmNetwork_CLI/main/Issue_3.PNG)
   
3. Configure the environment for the new user:
   ```bash
   (echo; echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"') >> /home/brewuser/.bashrc
   ```
4. Apply the changes:
   ```bash
   eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
   ```
   NB : If you found error like "Error: The current working directory must be readable to brewuser to run brew." you need to change the directory :
   ```bash
   cd ~
   eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
   ```
5. Install build essentials:
   ```bash
   sudo apt-get install build-essential
   ```
   
#### Installing Chasm Inference Scout:
Once you have Homebrew set up on your system, you can proceed with the installation of Chasm Inference Scout using the following commands:

1. Add the Chasm Network Tap
   First, we need to add the Chasm Network tap to Homebrew. A tap is a third-party repository for Homebrew formulas. Run the following command:
   ```bash
   brew tap ChasmNetwork/tap
   ```
   ![4](https://raw.githubusercontent.com/mumeido/ChasmNetwork_CLI/main/Issue_4.PNG)
   This command tells Homebrew to track the repository of Chasm Network, allowing you to install their custom packages.
2. Install Chasm CLI
   After adding the tap, you can install the Chasm CLI by running:
   ```bash
   brew install chasm-cli
   ```
   ![5](https://raw.githubusercontent.com/mumeido/ChasmNetwork_CLI/main/Issue_5.PNG)
   This command will download and install the Chasm Inference Scout CLI tool on your system.

#### Running Chasm CLI:
After successfully installing Chasm CLI, you can start using it by simply running the chasm command in your terminal. This command serves as the entry point for all Chasm-related operations. 
```bash
chasm
```
![5](https://raw.githubusercontent.com/mumeido/ChasmNetwork_CLI/main/Final.PNG)

Source : https://network-docs.chasm.net/chasm-scout-season-0/chasm-inference-scout-setup-guide/installing-chasm-inference-scout-via-cli






