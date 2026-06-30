# Get a Location

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0ZSUyRkxvY2F0aW9ucyUyRkdldCUyNTIwYSUyNTIwTG9jYXRpb24

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

[`LocationsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/locations-response-1.md)


# Example Usage

```ruby
id = 112

result = locations_controller.get_a_location(id)
puts result
```



