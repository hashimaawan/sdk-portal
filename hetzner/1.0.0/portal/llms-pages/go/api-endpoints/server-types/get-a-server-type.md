# Get a Server Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwVHlwZXMlMkZHZXQlMjUyMGElMjUyMFNlcnZlciUyNTIwVHlwZQ

Gets a specific Server type object.

:information_source: **Note** This endpoint does not require authentication.

```go
GetAServerType(
    ctx context.Context,
    id int) (
    models.ApiResponse[models.ServerTypesResponse1],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of Server Type |


# Response Type

**200**: The `server_type` key in the reply contains a Server type object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ServerTypesResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server-types-response-1.md).


# Example Usage

```go
ctx := context.Background()

id := 112

apiResponse, err := serverTypesController.GetAServerType(ctx, id)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```



