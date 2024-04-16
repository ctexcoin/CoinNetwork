# Run a CTEX Validator
## Setting up a node
1. Git clone https://github.com/ctexcoin/CoinNetwork.git

2. Copy source form node-example to root folder
```
cp -r CoinNetwork/node-example/CTEX  /root/
```
3. Create an Account

```
cd /root/CTEX
chmod +x openethereum
./openethereum account new --config nodes/validator/node.toml
```
Returned address like that 0x00aa39d30f0d20ff03a22ccfc30b7efbfca597c2

Copy result address to node.toml
Ex:
```
...
[account]
unlock = ["0x00aa39d30f0d20ff03a22ccfc30b7efbfca597c2"]
password = ["password"]

[mining]
force_sealing = true
engine_signer = "0x00aa39d30f0d20ff03a22ccfc30b7efbfca597c2"
reseal_on_txs = "none"
...
```
4. Run the authority nodes
```
./openethereum --config ./nodes/validator/node.toml

```
5. Stake

    Stake

    To stake CTEX coin, all you should do is sending your CTEX coin to the CTEX Consensus contract address over the CTEX network from the validator address.
    The CTEX Consensus contract address: 0x951d8D0849aE9bC906E7AB67b9d4BD2bf10B0132
    The easiest way to do so, is to import your private key or key-store file to your favourite wallet (for example Metamask), switch network to CTEX and send the CTEX coin to the Consensus contract address.

    You can find your key-store (containing your private key) and the password for the created account in:
    /CTEX/nodes/validator/keys/CTEX/UTC--xxxx
    /CTEX/nodes/validator/node.pwd

6. Wait for 1 cycle (approximately 48 hours).

    Wait until the next cycle gets started.

7. Clone this Repositry

git clone https://github.com/ctexcoin/eth-net-intelligence-api/blob/main/eth-net-intelligence-api.zip

8. Run Command apt get install

9. Go to Directory Run Command cd/eth-net-intelligence-api

10. Run command pm2 start app1.json
