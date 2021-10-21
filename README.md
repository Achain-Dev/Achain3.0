# Achain


### what's the Achain

Achain Smart Chain starts its development based on go-ethereum fork. So you may see many toolings, binaries and also docs are based on Ethereum ones, such as the name “geth”.

But from that baseline of EVM compatible, Achain Smart Chain introduces a system of 21 validators with Proof of Staked Authority (PoSA) consensus that can support short block time and lower fees. The most bonded validator candidates of staking will become validators and produce blocks. The double-sign detection and other slashing logic guarantee security, stability, and chain finality.

### Building the source

Many of the below are the same as or similar to go-ethereum.

For prerequisites and detailed build instructions please read the [Installation Instructions](https://github.com/ethereum/go-ethereum/wiki/Building-Ethereum) on the wiki.

Building `geth` requires both a Go (version 1.14 or later) and a C compiler. You can install
them using your favourite package manager. Once the dependencies are installed, run

```shell
make geth
```

or, to build the full suite of utilities:

```shell
make all
```

### How to run Full node

Steps:

1. Download the binary, config and genesis files from release, or compile the binary by make geth.
2. Init genesis state: ./geth --datadir node init genesis.json.
3. Start your fullnode: ./geth --datadir ./node --gcmode archive --networkid 59300 --bootnodes 'enode://1126d31cc48d3de8cc5195f57d462a0926cad3e1c892e2125060dfb1e6a125f6f0585f8e2557ee3deb50d56b232ec71a0c3836622279f543d3158dea6fc5f4c6@18.179.72.144:30303'
