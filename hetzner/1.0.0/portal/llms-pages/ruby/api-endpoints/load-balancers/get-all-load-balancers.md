# Get All Load Balancers

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRkdldCUyNTIwYWxsJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnM

Gets all existing Load Balancers that you have available.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_all_load_balancers(sort: nil,
                           name: nil,
                           label_selector: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`Sort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `name` | `String` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `label_selector` | `String` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `load_balancers` key contains a list of Load Balancers

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`LoadBalancersResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancers-response.md).


# Example Usage

```ruby
result = load_balancers_api.get_all_load_balancers

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



