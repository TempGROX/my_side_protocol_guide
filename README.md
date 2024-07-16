<div align=center>
  <img src="https://github.com/TempGROX/TempGROX/blob/main/src/photos/rounded-in-photoretrica%20(1).png" width="150">
</div>

<h1 align=center>my_side_protocol_guide</h1>
This repository contains my guide to the Side Protocol project node
<br>


# Download and Install
As always, let's first familiarize ourselves with the network parameters in the form of a handy sign!

|PARAMETR|VALUE|
|:-------|:----|
|**Chain ID**|grimoria-testnet-1|
|**RPC**|https://testnet-rpc.side.one|
|**Rest**|https://testnet-rest.side.one|
|**gRPC**|https://testnet-grpc.side.one:443|
|**Persistence Nodes**|6bef0693d7a31fed473b95123ad19b544b414093@202.182.119.24:26656,44f8009ed91fddd7ee51117482ede20fb4f33e78@149.28.156.79:26656|

## Hardware Requirement
Below are the minimum requirements for your system, if your requirements are lower, then you should not continue to follow this guide!

|PARAMETR|VALUE|
|:-------|:----|
|**CPU**|4 cores|
|**RAM**|8 GB|
|**Storage**|500 GB|
|**Network**|1 Gbps|

## Build from source code
```bash
git clone https://github.com/sideprotocol/side.git
cd side
git checkout v0.9.0
```

## Compile binary
```bash
make install
```

```bash
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
```
```bash
sided version
# 0.9.0
```

# Run Node
## Add key
```bash
sided keys add test --key-type="segwit"
```

## Initialize
```bash
sided init <MY_SIDE_VALIDATOR> --chain-id=grimoria-testnet-1
```

## Install Genesis file
```bash
wget https://raw.githubusercontent.com/sideprotocol/testnet/main/grimoria-testnet-1/genesis.json -O $HOME/.side/config/genesis.json
```

## Configure seeds and peers
```bash
cd $HOME/.side/config
nano config.toml

persistent_peers = "6bef0693d7a31fed473b95123ad19b544b414093@202.182.119.24:26656,44f8009ed91fddd7ee51117482ede20fb4f33e78@149.28.156.79:26656"
```

## Setup minimum gas price
```bash
minimum-gas-prices = "0.005uside"
```

# Start TestNet
```bash
sided tendermint unsafe-reset-all 
sided start
```

# The end!
If you liked this guide, please go to all my social networks)

<br>
<div id="badges" align="center">
  <a href="https://discord.com/users/961408999411048461">
    <img src="https://img.shields.io/badge/Discord-blue?style=for-the-badge&logo=https%3A%2F%2Fimg.icons8.com%2Fios%2F50%2Fmedium-logo.png&logoColor=white" alt="LinkedIn Badge"/>
  </a>
  <a href="https://medium.com/@James_Brandon">
    <img src="https://img.shields.io/badge/Medium-black?style=for-the-badge&logo=https%3A%2F%2Fimg.icons8.com%2Fios%2F50%2Fmedium-logo.png&logoColor=white" alt="Youtube Badge"/>
  </a>
  <a href="https://keybase.io/jamesbrandon">
    <img src="https://img.shields.io/badge/Keybase-orange?style=for-the-badge&logo=https%3A%2F%2Fimg.icons8.com%2Fios%2F50%2Fmedium-logo.png&logoColor=white">
  </a>
  <a href="https://x.com/JBTGrox">
    <img src="https://img.shields.io/badge/Twitter-blue?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter Badge"/>
  </a>
  <a href="https://linktr.ee/JBrandon_?utm_source=linktree_admin_share">
    <img src="https://img.shields.io/badge/Linktree-green?style=for-the-badge&logo=https%3A%2F%2Fimg.icons8.com%2Fios%2F50%2Fmedium-logo.png&logoColor=white">
  </a>
</div>
