# Get a Location

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkxvY2F0aW9ucyUyRkdldCUyNTIwYSUyNTIwTG9jYXRpb24

Returns a specific Location object.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_a_location(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of Location |


# Response Type

**200**: The `location` key in the reply contains a Location object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`LocationsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/locations-response-1.md).


# Example Usage

```ruby
id = 112

result = locations_api.get_a_location(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



