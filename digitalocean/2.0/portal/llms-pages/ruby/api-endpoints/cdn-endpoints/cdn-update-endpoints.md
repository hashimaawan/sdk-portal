# Cdn Update Endpoints

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRkNETiUyNTIwRW5kcG9pbnRzJTJGY2RuX3VwZGF0ZV9lbmRwb2ludHM

To update the TTL, certificate ID, or the FQDN of the custom subdomain for
an existing CDN endpoint, send a PUT request to
`/v2/cdn/endpoints/$ENDPOINT_ID`.

```ruby
def cdn_update_endpoints(cdn_id,
                         body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cdn_id` | `UUID \| String` | Template, Required | A unique identifier for a CDN endpoint. |
| `body` | [`V2CdnEndpointsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-cdn-endpoints-request.md) | Body, Required | - |


# Response Type

**200**: The response will be a JSON object with an `endpoint` key. This will be set to an object containing the standard CDN endpoint attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`V2CdnEndpointsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-cdn-endpoints-response-1.md).


# Example Usage

```ruby
cdn_id = '19f06b6a-3ace-4315-b086-499a0e521b76'

body = V2CdnEndpointsRequest.new(
  certificate_id: '892071a0-bb95-49bc-8021-3afd67a210bf',
  custom_domain: 'static.example.com',
  ttl: Ttl::ENUM_3600
)

result = cdn_endpoints_api.cdn_update_endpoints(
  cdn_id,
  body
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Example Response *(as JSON)*

```json
{
  "endpoint": {
    "created_at": "2018-07-19T15:04:16Z",
    "endpoint": "static-images.nyc3.cdn.digitaloceanspaces.com",
    "id": "19f06b6a-3ace-4315-b086-499a0e521b76",
    "origin": "static-images.nyc3.digitaloceanspaces.com",
    "ttl": 3600
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |



