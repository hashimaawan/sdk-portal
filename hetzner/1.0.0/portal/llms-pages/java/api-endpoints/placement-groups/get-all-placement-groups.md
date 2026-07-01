# Get All Placement Groups

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGR2V0JTI1MjBhbGwlMjUyMFBsYWNlbWVudEdyb3Vwcw

Returns all PlacementGroup objects.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<PlacementGroupsResponse>> getAllPlacementGroupsAsync(
    final Sort sort,
    final String name,
    final String labelSelector,
    final ParameterType1 type)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`Sort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `name` | `String` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `String` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `type` | [`ParameterType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/parameter-type-1.md) | Query, Optional | Can be used multiple times. The response will only contain PlacementGroups matching the type. |


# Response Type

**200**: The `placement_groups` key contains an array of PlacementGroup objects

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`PlacementGroupsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/placement-groups-response.md).


# Example Usage

```java
placementGroupsApi.getAllPlacementGroupsAsync(null, null, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Example Response *(as JSON)*

```json
{
  "placement_groups": [
    {
      "created": "2019-01-08T12:10:00+00:00",
      "id": 897,
      "labels": {
        "key": "value"
      },
      "name": "my Placement Group",
      "servers": [
        4711,
        4712
      ],
      "type": "spread"
    }
  ]
}
```



