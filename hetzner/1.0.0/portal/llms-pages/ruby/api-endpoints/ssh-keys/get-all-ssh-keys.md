# Get All SSH Keys

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkdldCUyNTIwYWxsJTI1MjBTU0glMjUyMGtleXM

Returns all SSH key objects.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_all_ssh_keys(sort: nil,
                     name: nil,
                     fingerprint: nil,
                     label_selector: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`Sort8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/sort-8.md) | Query, Optional | Can be used multiple times. |
| `name` | `String` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `fingerprint` | `String` | Query, Optional | Can be used to filter SSH keys by their fingerprint. The response will only contain the SSH key matching the specified fingerprint. |
| `label_selector` | `String` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `ssh_keys` key in the reply contains an array of SSH key objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`SshKeysResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/ssh-keys-response.md).


# Example Usage

```ruby
result = ssh_keys_api.get_all_ssh_keys

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



