# Update an SSH Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRlVwZGF0ZSUyNTIwYW4lMjUyMFNTSCUyNTIwa2V5

Updates an SSH key. You can update an SSH key name and an SSH key labels.

Please note that when updating labels, the SSH key current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

:information_source: **Note** This endpoint does not require authentication.

```python
def update_an_ssh_key(self,
                     id,
                     body=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `str` | Template, Required | ID of the SSH key |
| `body` | [`SshKeysRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/ssh-keys-request-1.md) | Body, Optional | - |


# Response Type

**200**: The `ssh_key` key in the reply contains the modified SSH key object with the new description

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`SshKeysResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/ssh-keys-response-1.md).


# Example Usage

```python
id = 'id0'

body = SshKeysRequest1(
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='My ssh key'
)

result = ssh_keys_api.update_an_ssh_key(
    id,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response *(as JSON)*

```json
{
  "ssh_key": {
    "created": "2016-01-30T23:50:00+00:00",
    "fingerprint": "b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f",
    "id": 2323,
    "labels": {
      "labelkey": "value"
    },
    "name": "My ssh key",
    "public_key": "ssh-rsa AAAjjk76kgf...Xt"
  }
}
```



