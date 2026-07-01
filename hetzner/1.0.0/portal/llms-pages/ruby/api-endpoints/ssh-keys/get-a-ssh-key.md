# Get a SSH Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkdldCUyNTIwYSUyNTIwU1NIJTI1MjBrZXk

Returns a specific SSH key object.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_a_ssh_key(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the SSH key |


# Response Type

**200**: The `ssh_key` key in the reply contains an SSH key object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`SshKeysResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/ssh-keys-response-1.md).


# Example Usage

```ruby
id = 112

result = ssh_keys_api.get_a_ssh_key(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



