# Create a Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0ZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGQ3JlYXRlJTI1MjBhJTI1MjBQbGFjZW1lbnRHcm91cA

Creates a new PlacementGroup.

:information_source: **Note** This endpoint does not require authentication.

```go
CreateAPlacementGroup(
    ctx context.Context,
    body *models.CreatePlacementGroupRequest) (
    models.ApiResponse[models.CreatePlacementGroupResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`*models.CreatePlacementGroupRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/create-placement-group-request.md) | Body, Optional | - |


# Response Type

**201**: The `PlacementGroup` key contains the PlacementGroup that was just created.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.CreatePlacementGroupResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/create-placement-group-response.md).


# Example Usage

```go
ctx := context.Background()

body := models.CreatePlacementGroupRequest{
    Name:                 "my Placement Group",
    Type:                 "spread",
}

apiResponse, err := placementGroupsController.CreateAPlacementGroup(ctx, &body)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Example Response *(as JSON)*

```json
{
  "placement_group": {
    "created": "2019-01-08T12:10:00+00:00",
    "id": 897,
    "labels": {
      "key": "value"
    },
    "name": "my Placement Group",
    "servers": [],
    "type": "spread"
  }
}
```



