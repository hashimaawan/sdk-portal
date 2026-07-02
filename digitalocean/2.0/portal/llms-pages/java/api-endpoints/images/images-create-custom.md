# Images Create Custom

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkltYWdlcyUyRmltYWdlc19jcmVhdGVfY3VzdG9t

To create a new custom image, send a POST request to /v2/images.
The body must contain a url attribute pointing to a Linux virtual machine
image to be imported into DigitalOcean.
The image must be in the raw, qcow2, vhdx, vdi, or vmdk format.
It may be compressed using gzip or bzip2 and must be smaller than 100 GB after
being decompressed.

```java
CompletableFuture<ApiResponse<V2ImagesResponse1>> imagesCreateCustomAsync(
    final V2ImagesRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V2ImagesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-images-request.md) | Body, Required | - |


# Response Type

**202**: The response will be a JSON object with a key set to `image`.  The value of this will be an image object containing a subset of the standard  image attributes as listed below, including the image's `id` and `status`.  After initial creation, the `status` will be `NEW`. Using the image's id, you  may query the image's status by sending a `GET` request to the  `/v2/images/$IMAGE_ID` endpoint.  When the `status` changes to `available`, the image will be ready for use.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`V2ImagesResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-images-response-1.md).


# Example Usage

```java
V2ImagesRequest body = new V2ImagesRequest.Builder(
    "ubuntu-18.04-minimal",
    Region2.NYC3,
    "http://cloud-images.ubuntu.com/minimal/releases/bionic/release/ubuntu-18.04-minimal-cloudimg-amd64.img"
)
.description("Cloud-optimized image w/ small footprint")
.distribution(Distribution.UBUNTU)
.tags(Arrays.asList(
        "base-image",
        "prod"
    ))
.build();

imagesApi.imagesCreateCustomAsync(body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof V21Clicks401ErrorException) {
        V21Clicks401ErrorException v21Clicks401ErrorException = (V21Clicks401ErrorException) cause;
        v21Clicks401ErrorException.printStackTrace();
    } else {
        // fallback for unexpected errors
        exception.printStackTrace();
    }

    return null;
});
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



