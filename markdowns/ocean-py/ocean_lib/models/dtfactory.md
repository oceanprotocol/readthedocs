---
title: dtfactory
slug: ocean_lib/models/dtfactory
app: ocean.py
module: ocean_lib.models.dtfactory
source: https://github.com/oceanprotocol/ocean.py/blob/main/ocean_lib/models/dtfactory.py
version: 0.5.30
---
## DTFactory

```python
@enforce_types
class DTFactory(ContractBase)
```

#### verify\_data\_token

```python
 | def verify_data_token(dt_address: str) -> bool
```

Checks that a token was registered.

#### get\_token\_registered\_event

```python
 | def get_token_registered_event(from_block: int, to_block: int, token_address: str) -> Optional[AttributeDict]
```

Retrieves event log of token registration.

#### get\_token\_minter

```python
 | def get_token_minter(token_address: str) -> str
```

Retrieves token minter.

This function will be deprecated in the next major release.
It's only kept for backwards compatibility.

#### get\_token\_address

```python
 | def get_token_address(transaction_id: str) -> str
```

Gets token address using transaction id.

