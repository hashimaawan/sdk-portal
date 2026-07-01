# Create a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRkNyZWF0ZSUyNTIwYSUyNTIwRmlyZXdhbGw

Creates a new Firewall.

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `server_already_added`        | Server added more than one time to resource                   |
| `incompatible_network_type`   | The Network type is incompatible for the given resource       |
| `firewall_resource_not_found` | The resource the Firewall should be attached to was not found |

:information_source: **Note** This endpoint does not require authentication.

```go
CreateAFirewall(
    ctx context.Context,
    body *models.CreateFirewallRequest) (
    models.ApiResponse[models.CreateFirewallResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`*models.CreateFirewallRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/create-firewall-request.md) | Body, Optional | - |


# Response Type

**201**: The `firewall` key contains the Firewall that was just created

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.CreateFirewallResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/create-firewall-response.md).


# Example Usage

```go
ctx := context.Background()

body := models.CreateFirewallRequest{
    ApplyTo:              []models.ApplyTo{
        models.ApplyTo{
            Server:               models.ToPointer(models.Server2{
                Id:                   42,
            }),
            Type:                 models.Type7Enum_SERVER,
        },
    },
    Labels:               models.ToPointer(interface{}("[env, dev]")),
    Name:                 "Corporate Intranet Protection",
    Rules:                []models.Rule{
        models.Rule{
            Description:          models.NewOptional(models.ToPointer("Allow port 80")),
            Direction:            models.DirectionEnum_IN,
            Port:                 models.ToPointer("80"),
            Protocol:             models.ProtocolEnum_TCP,
            SourceIps:            []string{
                "28.239.13.1/32",
                "28.239.14.0/24",
                "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
            },
        },
    },
}

apiResponse, err := firewallsController.CreateAFirewall(ctx, &body)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```



