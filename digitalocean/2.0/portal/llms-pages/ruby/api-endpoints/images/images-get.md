# Images Get

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRkltYWdlcyUyRmltYWdlc19nZXQ

To retrieve information about an image, send a `GET` request to
`/v2/images/$IDENTIFIER`.

```ruby
def images_get(image_id)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image_id` | Integer \| String | Template, Required | This is a container for any-of cases. |


# Response Type

**200**: The response will be a JSON object with a key called `image`.  The value of this will be an image object containing the standard image attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`V2ImagesResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-images-response-2.md).


# Example Usage

```ruby
image_id = 62137902

result = images_api.images_get(image_id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Example Response *(as JSON)*

```json
{
  "image": {
    "created_at": "2014-10-17T20:24:33Z",
    "description": "",
    "distribution": "Ubuntu",
    "error_message": "",
    "id": 6918990,
    "min_disk_size": 20,
    "name": "14.04 x64",
    "public": true,
    "regions": [
      "nyc1",
      "ams1",
      "sfo1",
      "nyc2",
      "ams2",
      "sgp1",
      "lon1",
      "nyc3",
      "ams3",
      "nyc3"
    ],
    "size_gigabytes": 2.34,
    "slug": "ubuntu-16-04-x64",
    "status": "available",
    "tags": []
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



