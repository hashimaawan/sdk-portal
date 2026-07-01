# Get All Datacenters

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRkRhdGFjZW50ZXJzJTJGR2V0JTI1MjBhbGwlMjUyMERhdGFjZW50ZXJz

Returns all Datacenter objects.

:information_source: **Note** This endpoint does not require authentication.

```go
GetAllDatacenters(
    ctx context.Context,
    name *string) (
    models.ApiResponse[models.DatacentersResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `*string` | Query, Optional | Can be used to filter Datacenters by their name. The response will only contain the Datacenter matching the specified name. When the name does not match the Datacenter name format, an `invalid_input` error is returned. |


# Response Type

**200**: The reply contains the `datacenters` and `recommendation` keys

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.DatacentersResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/datacenters-response.md).


# Example Usage

```go
ctx := context.Background()

apiResponse, err := datacentersApi.GetAllDatacenters(ctx, nil)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```



