# Get All Load Balancer Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyRkdldCUyNTIwYWxsJTI1MjBMb2FkJTI1MjBCYWxhbmNlciUyNTIwVHlwZXM

Gets all Load Balancer type objects.

:information_source: **Note** This endpoint does not require authentication.

```go
GetAllLoadBalancerTypes(
    ctx context.Context,
    name *string) (
    models.ApiResponse[models.LoadBalancerTypesResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `*string` | Query, Optional | Can be used to filter Load Balancer types by their name. The response will only contain the Load Balancer type matching the specified name. |


# Response Type

**200**: The `load_balancer_types` key in the reply contains an array of Load Balancer type objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.LoadBalancerTypesResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/load-balancer-types-response.md).


# Example Usage

```go
ctx := context.Background()

apiResponse, err := loadBalancerTypesController.GetAllLoadBalancerTypes(ctx, nil)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```



