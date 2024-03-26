# Command Line Interface for mining Orange

Python & Pip are required for this CLI to work.

Fill out **MINER_MNEMONIC** and **DEPOSIT_ADDRESS** fields in `.env` (deposit mnemonic is optional, only if you want to opt in through the CLI - not implemented yet).

Install requirements:

`pip install -r requirements.txt`

To start mining, use the CLI like this:

`python main.py testnet --tpm 60 --fee 2000`

```
tpm - transactions per minute
fee - fee per transaction in micro ALGO
```

# Run node

```
docker run --rm -it --name algo-node -p 8080:8080 -e NETWORK=mainnet -e FAST_CATCHUP=1 -e PROFILE=participation -v c:/temp/algorand:/algod/data --dns 8.8.8.8 algorand/algod:stable
```
