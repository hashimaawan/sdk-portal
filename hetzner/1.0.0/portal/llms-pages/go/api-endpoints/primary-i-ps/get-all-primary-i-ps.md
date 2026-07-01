# Get All Primary I Ps

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRkdldCUyNTIwYWxsJTI1MjBQcmltYXJ5JTI1MjBJUHM

Returns all Primary IP objects.

:information_source: **Note** This endpoint does not require authentication.

```go
GetAllPrimaryIPs(
    ctx context.Context,
    name *string,
    labelSelector *string,
    ip *string,
    sort *models.Sort2) (
    models.ApiResponse[models.PrimaryIPsResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `*string` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `*string` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `ip` | `*string` | Query, Optional | Can be used to filter resources by their ip. The response will only contain the resources matching the specified ip. |
| `sort` | [`*models.Sort2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/sort-2.md) | Query, Optional | Can be used multiple times. Choices id id:asc id:desc created created:asc created:desc |


# Response Type

**200**: The `primary_ips` key contains an array of Primary IP objects

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.PrimaryIPsResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/primary-i-ps-response.md).


# Example Usage

```go
ctx := context.Background()

ip := "127.0.0.1"

apiResponse, err := primaryIPsApi.GetAllPrimaryIPs(ctx, nil, nil, &ip, nil)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```



