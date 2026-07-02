# Images Update

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkltYWdlcyUyRmltYWdlc191cGRhdGU

To update an image, send a `PUT` request to `/v2/images/$IMAGE_ID`.
Set the `name` attribute to the new value you would like to use.
For custom images, the `description` and `distribution` attributes may also be updated.

```python
def images_update(self,
                 image_id,
                 body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image_id` | `int` | Template, Required | A unique number that can be used to identify and reference a specific image. |
| `body` | [`V2ImagesRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-images-request-1.md) | Body, Required | - |


# Response Type

**200**: The response will be a JSON object with a key set to `image`.  The value of this will be an image object containing the standard image attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`V2ImagesResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-images-response-2.md).


# Example Usage

```python
image_id = 62137902

body = V2ImagesRequest1(
    distribution=Distribution.UBUNTU,
    name='Nifty New Snapshot'
)

result = images_api.images_update(
    image_id,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response *(as JSON)*

```json
{
  "image": {
    "created_at": "2014-11-14T16:44:03Z",
    "description": "",
    "distribution": "Ubuntu",
    "error_message": "",
    "id": 7938391,
    "min_disk_size": 20,
    "name": "new-image-name",
    "public": false,
    "regions": [
      "nyc3",
      "nyc3"
    ],
    "size_gigabytes": 2.34,
    "slug": null,
    "status": "available",
    "tags": []
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |



