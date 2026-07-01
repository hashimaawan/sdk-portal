# Get All Images

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkltYWdlcyUyRkdldCUyNTIwYWxsJTI1MjBJbWFnZXM

Returns all Image objects. You can select specific Image types only and sort the results by using URI parameters.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<ImagesResponse>> getAllImagesAsync(
    final Sort sort,
    final Type21 type,
    final Status23 status,
    final String boundTo,
    final Boolean includeDeprecated,
    final String name,
    final String labelSelector)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`Sort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `type` | [`Type21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-21.md) | Query, Optional | Can be used multiple times. |
| `status` | [`Status23`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/status-23.md) | Query, Optional | Can be used multiple times. The response will only contain Images matching the status. |
| `boundTo` | `String` | Query, Optional | Can be used multiple times. Server ID linked to the Image. Only available for Images of type `backup` |
| `includeDeprecated` | `Boolean` | Query, Optional | Can be used multiple times. |
| `name` | `String` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `String` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `images` key in the reply contains an array of Image objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ImagesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/images-response.md).


# Example Usage

```java
imagesApi.getAllImagesAsync(null, null, null, null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



