# Arbutrum Claim Bot

## Features

- Import wallets from privateKeys and seedPhrases.
- Receive token on different wallets.
    + If you do not need a tokens transfer after claim, then leave the address blank.
- Select different gasPrice/gasLimit on each wallet.
- Support different proxy and nodes.
    + Proxy:
        * *Format: `ip:port:username:password`*
        * *HTTP only. SOCKS not supported.*
    + Nodes:
        * *Supported all types - HTTP, WS, IPC.*

> **The bot is provided with a 3% commission.
> Transfer commission is automatic and sends to random wallets.
> No overlap between wallets.**

## Account preparation

1. Copy spreadsheet from this [example](https://docs.google.com/spreadsheets/d/19y2zmGv4v1oBl3JwqA3hNjAWkENzTA86IHy1HYCOIPQ/edit#gid=0) *(Select second sheet to see example)*
2. Fill table with your wallets and other data 
3. Download as CSV file (File->Download->CSV)

## Start bot

- Download latest .exe file for your OS from [realease](https://github.com/frendri/arbitrum-claim/releases/tag/release)
- Download config.yaml
- Create a folder and put the three files there:
  + config.yaml
  + accs.csv
  + exe file
- Run bot

## FAQ
**When you start bot, then it will show your config and start load wallets**

![alt example](https://img4.teletype.in/files/b1/02/b10202f2-64b4-46f4-a0ec-f250ba14dc06.png)

> If you see some errors, check descriptions and fix it.

**Then, when ready -> press `Enter` and bot will start work.**

![alt example](https://img4.teletype.in/files/f9/c8/f9c806ef-c8b4-488f-929d-652f82668301.png)

**Bot will check tokens on your accounts, skip the empty accounts, and the rest will start work**

![alt example](https://img3.teletype.in/files/62/9e/629e75cb-50bd-44f6-a506-86de0f495d73.jpeg)

> If you see this, then everything is okay, and the software works.
> The bot simulates a claim transaction and sends it when the claim starts.

![alt example](https://img2.teletype.in/files/92/d6/92d691e5-439d-41b1-8162-b25667190f86.png)

**When claim starts, bot will send the transactions.**

## Config setting
**You can customize the config to your liking.**
The config contains comments with descriptions for each parameter.
> Optimal config - in the release.

```yaml
explorer_url: "https://arbiscan.io"
claimer_address: "0x67a24CE4321aB3aF51c2D0a4801c3E111D88C9d9"
# Claimer address. No need to change
token_address: "0x912ce59144191c1204e64559fe8253a0e49e6548"
# Token address. No need to change

spam_txs: false
# Spam transactions, if false send only one. Not work in build early mode
spam_interval: 1000
# Interval between spam transactions. Not lower than 0. Integer milliseconds
build_early: true
# Prepare transactions before claim start. Not work with spam_txs
estimate_gas: true
# Estimate gas for transaction
estimate_only_one: true
# Estimate gas only for one transaction. Not work in spam_txs mode
estimate_interval: 0
# Interval between estimate gas transactions.
# Not lower than 0. Integer milliseconds
accs_file: "accs.csv"
# File with accounts.
```

## Contacts
**If you have any problems at startup, text me:**
[Telegram](https://t.me/frendri)
