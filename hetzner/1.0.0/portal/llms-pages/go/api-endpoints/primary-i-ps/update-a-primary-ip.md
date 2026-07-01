# Update a Primary IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRlVwZGF0ZSUyNTIwYSUyNTIwUHJpbWFyeSUyNTIwSVA

Updates the Primary IP.

Note that when updating labels, the Primary IP's current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

If the Primary IP object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```go
UpdateAPrimaryIp(
    ctx context.Context,
    id int,
    body *models.UpdatePrimaryIpRequest) (
    models.ApiResponse[models.PrimaryIpResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |
| `body` | [`*models.UpdatePrimaryIpRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/update-primary-ip-request.md) | Body, Optional | - |


# Response Type

**200**: The `primary_ip` key contains the Primary IP that was just updated

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.PrimaryIpResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/primary-ip-response.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.UpdatePrimaryIpRequest{
    AutoDelete:            models.ToPointer(true),
    Labels:                models.ToPointer(interface{}("[labelkey, value]")),
    Name:                  models.ToPointer("my-ip"),
}

apiResponse, err := primaryIPsApi.UpdateAPrimaryIp(ctx, id, &body)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```



