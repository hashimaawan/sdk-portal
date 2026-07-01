# Get All Locations

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkxvY2F0aW9ucyUyRkdldCUyNTIwYWxsJTI1MjBMb2NhdGlvbnM

Returns all Location objects.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<LocationsResponse>> getAllLocationsAsync(
    final String name)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Query, Optional | Can be used to filter Locations by their name. The response will only contain the Location matching the specified name. |


# Response Type

**200**: The `locations` key in the reply contains an array of Location objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`LocationsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/locations-response.md).


# Example Usage

```java
locationsApi.getAllLocationsAsync(null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



