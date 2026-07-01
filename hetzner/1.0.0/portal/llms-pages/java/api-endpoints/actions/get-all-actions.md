# Get All Actions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkFjdGlvbnMlMkZHZXQlMjUyMGFsbCUyNTIwQWN0aW9ucw

Returns all Action objects. You can `sort` the results by using the sort URI parameter, and filter them with the `status` parameter.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<ActionsResponse>> getAllActionsAsync(
    final Integer id,
    final ParameterSort sort,
    final ParameterStatus status)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Query, Optional | Can be used multiple times, the response will contain only Actions with specified IDs |
| `sort` | [`ParameterSort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/parameter-sort.md) | Query, Optional | Can be used multiple times. |
| `status` | [`ParameterStatus`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/parameter-status.md) | Query, Optional | Can be used multiple times, the response will contain only Actions with specified statuses |


# Response Type

**200**: The `actions` key contains a list of Actions

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/actions-response.md).


# Example Usage

```java
actionsApi.getAllActionsAsync(null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



