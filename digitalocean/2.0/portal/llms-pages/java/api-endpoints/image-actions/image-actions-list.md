# Image Actions List

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkltYWdlJTI1MjBBY3Rpb25zJTJGaW1hZ2VBY3Rpb25zX2xpc3Q

To retrieve all actions that have been executed on an image, send a GET request to `/v2/images/$IMAGE_ID/actions`.

```java
CompletableFuture<ApiResponse<V2ImagesActionsResponse>> imageActionsListAsync(
    final int imageId)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `imageId` | `int` | Template, Required | A unique number that can be used to identify and reference a specific image. |


# Response Type

**200**: The results will be returned as a JSON object with an `actions` key. This will be set to an array filled with action objects containing the standard action attributes.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`V2ImagesActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-images-actions-response.md).


# Example Usage

```java
int imageId = 62137902;

imageActionsApi.imageActionsListAsync(imageId).thenAccept(result -> {
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
  "actions": [
    {
      "completed_at": "2014-07-25T15:10:20Z",
      "id": 29410565,
      "region": {
        "available": true,
        "features": [
          "private_networking",
          "backups",
          "ipv6",
          "metadata",
          "server_id",
          "install_agent",
          "storage",
          "image_transfer"
        ],
        "name": "New York 2",
        "sizes": [
          "s-1vcpu-3gb",
          "m-1vcpu-8gb",
          "s-3vcpu-1gb",
          "s-1vcpu-2gb",
          "s-2vcpu-2gb",
          "s-2vcpu-4gb",
          "s-4vcpu-8gb",
          "s-6vcpu-16gb",
          "s-8vcpu-32gb",
          "s-12vcpu-48gb",
          "s-16vcpu-64gb",
          "s-20vcpu-96gb",
          "s-1vcpu-1gb",
          "c-1vcpu-2gb",
          "s-24vcpu-128gb"
        ],
        "slug": "nyc2"
      },
      "region_slug": "nyc2",
      "resource_id": 7555620,
      "resource_type": "image",
      "started_at": "2014-07-25T15:04:21Z",
      "status": "completed",
      "type": "transfer"
    }
  ],
  "links": {
    "pages": {
      "last": "https://api.digitalocean.com/v2/images/7555620/actions?page=5&per_page=1",
      "next": "https://api.digitalocean.com/v2/images/7555620/actions?page=2&per_page=1"
    }
  },
  "meta": {
    "total": 5
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



