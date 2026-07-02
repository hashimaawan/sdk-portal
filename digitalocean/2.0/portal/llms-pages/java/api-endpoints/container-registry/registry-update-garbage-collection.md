# Registry Update Garbage Collection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkNvbnRhaW5lciUyNTIwUmVnaXN0cnklMkZyZWdpc3RyeV91cGRhdGVfZ2FyYmFnZUNvbGxlY3Rpb24

To cancel the currently-active garbage collection for a registry, send a PUT request to `/v2/registry/$REGISTRY_NAME/garbage-collection/$GC_UUID` and specify one or more of the attributes below.

```java
CompletableFuture<ApiResponse<V2RegistryGarbageCollectionResponse>> registryUpdateGarbageCollectionAsync(
    final String registryName,
    final String garbageCollectionUuid,
    final V2RegistryGarbageCollectionRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `registryName` | `String` | Template, Required | The name of a container registry. |
| `garbageCollectionUuid` | `String` | Template, Required | The UUID of a garbage collection run. |
| `body` | [`V2RegistryGarbageCollectionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-registry-garbage-collection-request.md) | Body, Required | - |


# Response Type

**200**: The response will be a JSON object with a key of `garbage_collection`. This will be a json object with attributes representing the currently-active garbage collection.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`V2RegistryGarbageCollectionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-registry-garbage-collection-response.md).


# Example Usage

```java
String registryName = "example";
String garbageCollectionUuid = "eff0feee-49c7-4e8f-ba5c-a320c109c8a8";
V2RegistryGarbageCollectionRequest body = new V2RegistryGarbageCollectionRequest.Builder()
    .cancel(true)
    .build();

containerRegistryApi.registryUpdateGarbageCollectionAsync(registryName, garbageCollectionUuid, body).thenAccept(result -> {
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



