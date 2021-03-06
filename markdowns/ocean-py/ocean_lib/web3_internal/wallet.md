---
title: wallet
slug: ocean_lib/web3_internal/wallet
app: ocean.py
module: ocean_lib.web3_internal.wallet
source: https://github.com/oceanprotocol/ocean.py/blob/main/ocean_lib/web3_internal/wallet.py
version: 0.5.30
---
## Wallet

```python
@enforce_types
class Wallet()
```

The wallet is responsible for signing transactions and messages by using an account's
private key.

The use of this wallet allows Ocean tools to send rawTransactions which keeps the user
key and password safe and they are never sent outside. Another advantage of this is that
we can interact directly with remote network nodes without having to run a local parity
node since we only send the raw transaction hash so the user info is safe.

Usage:
    1. `wallet = Wallet(ocean.web3, private_key=private_key)`

#### \_\_init\_\_

```python
 | def __init__(web3: Web3, private_key: str) -> None
```

Initialises Wallet object.

#### sign

```python
 | def sign(msg_hash: SignableMessage) -> SignedMessage
```

Sign a transaction.

