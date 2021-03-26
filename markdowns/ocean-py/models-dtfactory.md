# Table of Contents

* [models.dtfactory](#models.dtfactory)
  * [DTFactory](#models.dtfactory.DTFactory)
    * [verify\_data\_token](#models.dtfactory.DTFactory.verify_data_token)
    * [get\_token\_registered\_event](#models.dtfactory.DTFactory.get_token_registered_event)
    * [get\_token\_minter](#models.dtfactory.DTFactory.get_token_minter)
    * [get\_token\_address](#models.dtfactory.DTFactory.get_token_address)

<a name="models.dtfactory"></a>
# models.dtfactory

<a name="models.dtfactory.DTFactory"></a>
## DTFactory Objects

```python
class DTFactory(ContractBase)
```

<a name="models.dtfactory.DTFactory.verify_data_token"></a>
#### verify\_data\_token

```python
 | verify_data_token(dt_address)
```

Checks that a token was registered.

<a name="models.dtfactory.DTFactory.get_token_registered_event"></a>
#### get\_token\_registered\_event

```python
 | get_token_registered_event(from_block, to_block, token_address)
```

Retrieves event log of token registration.

<a name="models.dtfactory.DTFactory.get_token_minter"></a>
#### get\_token\_minter

```python
 | get_token_minter(token_address)
```

Retrieves token minter.

This function will be deprecated in the next major release.
It's only kept for backwards compatibility.

<a name="models.dtfactory.DTFactory.get_token_address"></a>
#### get\_token\_address

```python
 | get_token_address(transaction_id: str) -> str
```

Gets token address using transaction id.
