# Update a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZVcGRhdGUlMjUyMGElMjUyMFNlcnZlcg

Updates a Server. You can update a Server’s name and a Server’s labels.
Please note that Server names must be unique per Project and valid hostnames as per RFC 1123 (i.e. may only contain letters, digits, periods, and dashes).
Also note that when updating labels, the Server’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

:information_source: **Note** This endpoint does not require authentication.

```go
UpdateAServer(
    ctx context.Context,
    id int,
    body *models.UpdateServerRequest) (
    models.ApiResponse[models.ServersResponse2],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`*models.UpdateServerRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/update-server-request.md) | Body, Optional | - |


# Response Type

**200**: The `server` key in the reply contains the updated Server

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ServersResponse2](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/servers-response-2.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.UpdateServerRequest{
    Labels:                models.ToPointer(interface{}("[labelkey, value]")),
    Name:                  models.ToPointer("my-server"),
}

apiResponse, err := serversApi.UpdateAServer(ctx, id, &body)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```



