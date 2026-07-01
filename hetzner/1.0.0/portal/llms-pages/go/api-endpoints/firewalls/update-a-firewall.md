# Update a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRlVwZGF0ZSUyNTIwYSUyNTIwRmlyZXdhbGw

Updates the Firewall.

Note that when updating labels, the Firewall's current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

Note: if the Firewall object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```go
UpdateAFirewall(
    ctx context.Context,
    id int,
    body *models.UpdateFirewallRequest) (
    models.ApiResponse[models.FirewallResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |
| `body` | [`*models.UpdateFirewallRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/update-firewall-request.md) | Body, Optional | - |


# Response Type

**200**: The `firewall` key contains the Firewall that was just updated

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.FirewallResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/firewall-response.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.UpdateFirewallRequest{
    Labels:               models.ToPointer(interface{}("[labelkey, value]")),
    Name:                 models.ToPointer("new-name"),
}

apiResponse, err := firewallsController.UpdateAFirewall(ctx, id, &body)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```



