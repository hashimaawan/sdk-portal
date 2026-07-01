# Create an SSH Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkNyZWF0ZSUyNTIwYW4lMjUyMFNTSCUyNTIwa2V5

Creates a new SSH key with the given `name` and `public_key`. Once an SSH key is created, it can be used in other calls such as creating Servers.

:information_source: **Note** This endpoint does not require authentication.

```python
def create_an_ssh_key(self,
                     body=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`SshKeysRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/ssh-keys-request.md) | Body, Optional | - |


# Response Type

**201**: The `ssh_key` key in the reply contains the object that was just created

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`SshKeysResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/ssh-keys-response-1.md).


# Example Usage

```python
body = SshKeysRequest(
    name='My ssh key',
    public_key='ssh-rsa AAAjjk76kgf...Xt'
)

result = ssh_keys_api.create_an_ssh_key(
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



