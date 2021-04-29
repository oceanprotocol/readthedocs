---
title: did
slug: /read-the-docs/provider/did
app: provider
module: common.did
---
DID Lib to do DID's and DDO's.

## DID

```python
class DID()
```

Class representing an asset DID.

#### did

```python
 | @staticmethod
 | def did(seed)
```

Create a did.

Format of the did:
did:op:cb36cf78d87f4ce4a784f17c2a4a694f19f3fbf05b814ac6b0b7197163888865

**Arguments**:

- `seed`: The list of checksums that is allocated in the proof, dict

**Returns**:

Asset did, str.

#### did\_parse

```python
def did_parse(did)
```

Parse a DID into it's parts.

**Arguments**:

- `did`: Asset did, str.

**Returns**:

Python dictionary with the method and the id.

#### is\_did\_valid

```python
def is_did_valid(did)
```

Did validator.

Return True if the did is a valid DID with the method name 'op' and the id
in the Ocean format

**Arguments**:

- `did`: Asset did, str
:return bool

#### id\_to\_did

```python
def id_to_did(did_id, method="op")
```

Return an Ocean DID from given a hex id.

#### did\_to\_id

```python
def did_to_id(did)
```

Return an id extracted from a DID string.

#### did\_to\_id\_bytes

```python
def did_to_id_bytes(did)
```

Return an Ocean DID to it's correspondng hex id in bytes.

So did:op:<hex>, will return <hex> in byte format
