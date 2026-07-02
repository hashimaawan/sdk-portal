# Droplets Destroy with Associated Resources Dangerous

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRkRyb3BsZXRzJTJGZHJvcGxldHNfZGVzdHJveV93aXRoQXNzb2NpYXRlZFJlc291cmNlc0Rhbmdlcm91cw

To destroy a Droplet along with all of its associated resources, send a DELETE
request to the `/v2/droplets/$DROPLET_ID/destroy_with_associated_resources/dangerous`
endpoint. The headers of this request must include an `X-Dangerous` key set to
`true`. To preview which resources will be destroyed, first query the
Droplet's associated resources. This operation _can not_ be reverse and should
be used with caution.

A successful response will include a 202 response code and no content. Use the
status endpoint to check on the success or failure of the destruction of the
individual resources.

```ruby
def droplets_destroy_with_associated_resources_dangerous(droplet_id,
                                                         x_dangerous)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet_id` | `Integer` | Template, Required | A unique identifier for a Droplet instance.<br><br>**Constraints**: `>= 1` |
| `x_dangerous` | `TrueClass \| FalseClass` | Header, Required | Acknowledge this action will destroy the Droplet and all associated resources and _can not_ be reversed. |


# Response Type

**202**: The does not indicate the success or failure of any operation, just that the request has been accepted for processing.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ruby
droplet_id = 3164444

x_dangerous = true

result = droplets_api.droplets_destroy_with_associated_resources_dangerous(
  droplet_id,
  x_dangerous
)

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



