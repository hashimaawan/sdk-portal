# Get All Volumes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlZvbHVtZXMlMkZHZXQlMjUyMGFsbCUyNTIwVm9sdW1lcw

Gets all existing Volumes that you have available.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_all_volumes(status: nil,
                    sort: nil,
                    name: nil,
                    label_selector: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`Status23`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/status-23.md) | Query, Optional | Can be used multiple times. The response will only contain Volumes matching the status. |
| `sort` | [`Sort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `name` | `String` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `label_selector` | `String` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `volumes` key contains a list of volumes

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`VolumesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/volumes-response.md).


# Example Usage

```ruby
result = volumes_api.get_all_volumes

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



