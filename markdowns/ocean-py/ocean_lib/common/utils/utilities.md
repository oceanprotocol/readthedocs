---
title: utilities
slug: ocean_lib/common/utils/utilities
app: ocean.py
module: ocean_lib.common.utils.utilities
source: https://github.com/oceanprotocol/ocean.py/blob/main/ocean_lib/common/utils/utilities.py
version: 0.5.30
---
Utilities class

#### generate\_new\_id

```python
def generate_new_id() -> str
```

Generate a new id without prefix.

**Returns**:

Id, str

#### to\_32byte\_hex

```python
def to_32byte_hex(val: Any) -> str
```

**Arguments**:

- `val`: 

**Returns**:



#### convert\_to\_bytes

```python
def convert_to_bytes(data: str) -> bytes
```

**Arguments**:

- `data`: 

**Returns**:



#### convert\_to\_string

```python
def convert_to_string(data: bytes) -> HexStr
```

**Arguments**:

- `data`: 

**Returns**:



#### convert\_to\_text

```python
def convert_to_text(data: bytes) -> str
```

**Arguments**:

- `data`: 

**Returns**:



#### checksum

```python
def checksum(seed: Dict[str, Any]) -> str
```

Calculate the hash3_256.

#### get\_timestamp

```python
def get_timestamp() -> str
```

Return the current system timestamp.

