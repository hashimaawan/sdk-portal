# Get All SSH Keys

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkdldCUyNTIwYWxsJTI1MjBTU0glMjUyMGtleXM

Returns all SSH key objects.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_all_ssh_keys(self,
                    sort=None,
                    name=None,
                    fingerprint=None,
                    label_selector=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`Sort8Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/sort-8.md) | Query, Optional | Can be used multiple times. |
| `name` | `str` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `fingerprint` | `str` | Query, Optional | Can be used to filter SSH keys by their fingerprint. The response will only contain the SSH key matching the specified fingerprint. |
| `label_selector` | `str` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `ssh_keys` key in the reply contains an array of SSH key objects with this structure

[`SshKeysResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/ssh-keys-response.md)


# Example Usage

```python
result = ssh_keys_controller.get_all_ssh_keys()
print(result)
```



