---
title: ddo
slug: None
app: ocean.py
module: ocean_lib.common.ddo.ddo
source: https://github.com/oceanprotocol/ocean.py/blob/main/ocean_lib/common/ddo/ddo.py
---
## DDO

```python
class DDO()
```

DDO class to create, import, export, validate DDO objects.

#### \_\_init\_\_

```python
 | def __init__(did=None, json_text=None, json_filename=None, created=None, dictionary=None)
```

Clear the DDO data values.

#### did

```python
 | @property
 | def did()
```

Get the DID.

#### is\_disabled

```python
 | @property
 | def is_disabled()
```

Returns whether the asset is disabled.

#### is\_enabled

```python
 | @property
 | def is_enabled()
```

Returns the opposite of is_disabled, for convenience.

#### asset\_id

```python
 | @property
 | def asset_id()
```

The asset id part of the DID

#### services

```python
 | @property
 | def services()
```

Get the list of services.

#### proof

```python
 | @property
 | def proof()
```

Get the static proof, or None.

#### credentials

```python
 | @property
 | def credentials()
```

Get the credentials.

#### metadata

```python
 | @property
 | def metadata()
```

Get the metadata service.

#### encrypted\_files

```python
 | @property
 | def encrypted_files()
```

Return encryptedFiles field in the base metadata.

#### add\_public\_key

```python
 | def add_public_key(did, public_key)
```

Add a public key object to the list of public keys.

**Arguments**:

- `public_key`: Public key, PublicKeyHex

#### add\_authentication

```python
 | def add_authentication(public_key, authentication_type)
```

Add a authentication public key id and type to the list of authentications.

**Arguments**:

- `public_key`: Key id, Authentication
- `authentication_type`: Authentication type, str

#### add\_service

```python
 | def add_service(service_type, service_endpoint=None, values=None, index=None)
```

Add a service to the list of services on the DDO.

**Arguments**:

- `service_type`: Service
- `service_endpoint`: Service endpoint, str
- `values`: Python dict with index, templateId, serviceAgreementContract,
list of conditions and purchase endpoint.

#### as\_text

```python
 | def as_text(is_proof=True, is_pretty=False)
```

Return the DDO as a JSON text.

:param if is_proof: if False then do not include the 'proof' element.

**Arguments**:

- `is_pretty`: If True return dictionary in a prettier way, bool

**Returns**:

str

#### as\_dictionary

```python
 | def as_dictionary(is_proof=True)
```

Return the DDO as a JSON dict.

:param if is_proof: if False then do not include the 'proof' element.

**Returns**:

dict

#### add\_proof

```python
 | def add_proof(checksums, publisher_account)
```

Add a proof to the DDO, based on the public_key id/index and signed with the private key
add a static proof to the DDO, based on one of the public keys.

**Arguments**:

- `checksums`: dict with the checksum of the main attributes of each service, dict
- `publisher_account`: account of the publisher, account

#### get\_public\_key

```python
 | def get_public_key(key_id)
```

Key_id can be a string, or int. If int then the index in the list of keys.

#### get\_service

```python
 | def get_service(service_type=None)
```

Return a service using.

#### get\_service\_by\_index

```python
 | def get_service_by_index(index)
```

Get service for a given index.

**Arguments**:

- `index`: Service id, str

**Returns**:

Service

#### public\_keys

```python
 | @property
 | def public_keys()
```

Get the list of public keys.

#### authentications

```python
 | @property
 | def authentications()
```

Get the list authentication records.

#### create\_public\_key\_from\_json

```python
 | @staticmethod
 | def create_public_key_from_json(values)
```

Create a public key object based on the values from the JSON record.

#### create\_authentication\_from\_json

```python
 | @staticmethod
 | def create_authentication_from_json(values)
```

Create authentication object from a JSON dict.

#### enable

```python
 | def enable()
```

Enables asset for ordering.

#### disable

```python
 | def disable()
```

Disables asset from ordering.

#### requires\_address\_credential

```python
 | @property
 | def requires_address_credential()
```

Checks if an address credential is required on this asset.

#### allowed\_addresses

```python
 | @property
 | def allowed_addresses()
```

Lists addresses that are explicitly allowed in credentials.

#### denied\_addresses

```python
 | @property
 | def denied_addresses()
```

Lists addresesses that are explicitly denied in credentials.

#### add\_address\_to\_allow\_list

```python
 | def add_address_to_allow_list(address)
```

Adds an address to allowed addresses list.

#### add\_address\_to\_deny\_list

```python
 | def add_address_to_deny_list(address)
```

Adds an address to the denied addresses list.

#### remove\_address\_from\_allow\_list

```python
 | def remove_address_from_allow_list(address)
```

Removes address from allow list (if it exists).

#### remove\_address\_from\_deny\_list

```python
 | def remove_address_from_deny_list(address)
```

Removes address from deny list (if it exists).

#### is\_consumable

```python
 | def is_consumable(credential=None, with_connectivity_check=True, provider_uri=None)
```

Checks whether an asset is consumable and returns a ConsumableCode.
