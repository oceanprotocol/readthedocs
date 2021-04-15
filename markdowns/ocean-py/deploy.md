---
title: deploy
slug: /read-the-docs/ocean-py/deploy
section: ocean.py
sub_section: ocean_lib.ocean
---
Used for deploying fake OCEAN
isort:skip_file

#### deploy\_fake\_OCEAN

```python
def deploy_fake_OCEAN()
```

Does the following:
1. Deploy to ganache a new ERC20 contract having symbol OCEAN
2. Mints tokens
3. Distributes tokens to TEST_PRIVATE_KEY1 and TEST_PRIVATE_KEY2
4. In addresses.json, updates development : Ocean entry with new address
