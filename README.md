# Tinybird <3 Ethereum 



## Steps 

1. Create an account in https://www.tinybird.co/ if you don't have one
2. Install the tinybird cli `pip install tinybird-cli`. [More information here](https://docs.tinybird.co/cli.html)  
3. Clone this repository `git clone https://github.com/alexon1234/ethereum_tinybird.git`
4. Authentificate yourself using the token from the tinybird dashboard
```
    cd ethereum_tinybird
    tb auth
```

5. Download the data from [here](https://drive.google.com/file/d/1t7RR2rAsugM2iq0q21KnxlRp5El0Aki1/view?usp=sharing) or you can download the csv from this [kaggle's notebook](https://www.kaggle.com/alexdelamo/ethereum-transactions-january-2021) and extract it into `/datasource/fixtures`.

    In case you want to download the data from Kaggle, you need to download the following csv's/gz:
    - From the input section, you need to download `ETH_USD.csv`
    - From the output section, you need to download `tokens.csv`, `token_transactions.csv.gz` and `transactions.csv.gz`
    - Extract the compress files and place them into `/datasource/fixtures`

6. Once you have all the data, your directory should look like this

```
├── README.md
├── datasources
│   ├── ETH_USD.datasource
│   ├── blocks.datasource
│   ├── fixtures
│   │   ├── ETH_USD.csv
│   │   ├── blocks.csv
│   │   ├── token_transactions.csv
│   │   ├── tokens.csv
│   │   └── transactions.csv
│   ├── token_transactions.datasource
│   ├── tokens.datasource
│   └── transactions.datasource
├── endpoints
├── explorations
└── pipes
    └── Analyzing_Ethereum_blockchain.pipe
```

7. Create everything by just running `tb push --push-deps --fixtures`
