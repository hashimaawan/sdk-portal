# Delete a Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGRGVsZXRlJTI1MjBhJTI1MjBQbGFjZW1lbnRHcm91cA

Deletes a PlacementGroup.

:information_source: **Note** This endpoint does not require authentication.

```go
DeleteAPlacementGroup(
    ctx context.Context,
    id int) (
    http.Response,
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**204**: PlacementGroup deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```go
ctx := context.Background()

id := 112

resp, err := placementGroupsApi.DeleteAPlacementGroup(ctx, id)
if err != nil {
    log.Fatalln(err)
} else {
    fmt.Println(resp.StatusCode)
}
```



