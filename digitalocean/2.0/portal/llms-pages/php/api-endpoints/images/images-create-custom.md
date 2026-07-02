# Images Create Custom

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkltYWdlcyUyRmltYWdlc19jcmVhdGVfY3VzdG9t

To create a new custom image, send a POST request to /v2/images.
The body must contain a url attribute pointing to a Linux virtual machine
image to be imported into DigitalOcean.
The image must be in the raw, qcow2, vhdx, vdi, or vmdk format.
It may be compressed using gzip or bzip2 and must be smaller than 100 GB after
being decompressed.

```php
function imagesCreateCustom(V2ImagesRequest $body): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V2ImagesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-images-request.md) | Body, Required | - |


# Response Type

**202**: The response will be a JSON object with a key set to `image`.  The value of this will be an image object containing a subset of the standard  image attributes as listed below, including the image's `id` and `status`.  After initial creation, the `status` will be `NEW`. Using the image's id, you  may query the image's status by sending a `GET` request to the  `/v2/images/$IMAGE_ID` endpoint.  When the `status` changes to `available`, the image will be ready for use.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2ImagesResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-images-response-1.md).


# Example Usage

```php
$body = V2ImagesRequestBuilder::init(
    'ubuntu-18.04-minimal',
    Region2::NYC3,
    'http://cloud-images.ubuntu.com/minimal/releases/bionic/release/ubuntu-18.04-minimal-cloudimg-amd64.img'
)
    ->description('Cloud-optimized image w/ small footprint')
    ->distribution(Distribution::UBUNTU)
    ->tags(
        [
            'base-image',
            'prod'
        ]
    )
    ->build();

$imagesApi = $client->getImagesApi();
$apiResponse = $imagesApi->imagesCreateCustom($body);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2ImagesResponse1:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "image": {
    "created_at": "2018-09-20T19:28:00Z",
    "description": "Cloud-optimized image w/ small footprint",
    "distribution": "Ubuntu",
    "error_message": "",
    "id": 38413969,
    "name": "ubuntu-18.04-minimal",
    "regions": [],
    "status": "NEW",
    "tags": [
      "base-image",
      "prod"
    ],
    "type": "custom"
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |



