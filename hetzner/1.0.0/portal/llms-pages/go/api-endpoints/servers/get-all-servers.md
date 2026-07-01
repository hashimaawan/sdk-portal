# Get All Servers

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZHZXQlMjUyMGFsbCUyNTIwU2VydmVycw

Returns all existing Server objects

:information_source: **Note** This endpoint does not require authentication.

```go
GetAllServers(
    ctx context.Context,
    name *string,
    labelSelector *string,
    sort *models.Sort,
    status *models.Status70) (
    models.ApiResponse[models.ServersResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `*string` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `*string` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `sort` | [`*models.Sort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `status` | [`*models.Status70`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/status-70.md) | Query, Optional | Can be used multiple times. The response will only contain Server matching the status |


# Response Type

**200**: A paged array of servers

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ServersResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/servers-response.md).


# Example Usage

```go
ctx := context.Background()

apiResponse, err := serversApi.GetAllServers(ctx, nil, nil, nil, nil)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```



