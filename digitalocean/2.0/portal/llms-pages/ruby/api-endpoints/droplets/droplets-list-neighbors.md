# Droplets List Neighbors

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRkRyb3BsZXRzJTJGZHJvcGxldHNfbGlzdF9uZWlnaGJvcnM

To retrieve a list of any "neighbors" (i.e. Droplets that are co-located on
the same physical hardware) for a specific Droplet, send a GET request to
`/v2/droplets/$DROPLET_ID/neighbors`.

The results will be returned as a JSON object with a key of `droplets`. This
will be set to an array containing objects representing any other Droplets
that share the same physical hardware. An empty array indicates that the
Droplet is not co-located any other Droplets associated with your account.

```ruby
def droplets_list_neighbors(droplet_id)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet_id` | `Integer` | Template, Required | A unique identifier for a Droplet instance.<br><br>**Constraints**: `>= 1` |


# Response Type

**200**: A JSON object with an `droplets` key.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`V2DropletsNeighborsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-droplets-neighbors-response.md).


# Example Usage

```ruby
droplet_id = 3164444

result = droplets_api.droplets_list_neighbors(droplet_id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |



