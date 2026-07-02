# Cdn Purge Cache

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkNETiUyNTIwRW5kcG9pbnRzJTJGY2RuX3B1cmdlX2NhY2hl

To purge cached content from a CDN endpoint, send a DELETE request to
`/v2/cdn/endpoints/$ENDPOINT_ID/cache`. The body of the request should include
a `files` attribute containing a list of cached file paths to be purged. A
path may be for a single file or may contain a wildcard (`*`) to recursively
purge all files under a directory. When only a wildcard is provided, all
cached files will be purged. There is a rate limit of 50 files per 20 seconds
that can be purged.

```java
CompletableFuture<ApiResponse<Void>> cdnPurgeCacheAsync(
    final UUID cdnId,
    final V2CdnEndpointsCacheRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cdnId` | `UUID` | Template, Required | A unique identifier for a CDN endpoint. |
| `body` | [`V2CdnEndpointsCacheRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-cdn-endpoints-cache-request.md) | Body, Required | - |


# Response Type

**204**: The action was successful and the response body is empty.

`void`


# Example Usage

```java
UUID cdnId = UUID.fromString("19f06b6a-3ace-4315-b086-499a0e521b76");
V2CdnEndpointsCacheRequest body = new V2CdnEndpointsCacheRequest.Builder(
    Arrays.asList(
        "path/to/image.png",
        "path/to/css/*"
    )
)
.build();

cdnEndpointsApi.cdnPurgeCacheAsync(cdnId, body).thenAccept(result -> {
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


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



