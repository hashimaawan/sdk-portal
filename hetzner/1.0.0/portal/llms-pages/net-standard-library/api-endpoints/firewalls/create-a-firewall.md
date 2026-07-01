# Create a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRkNyZWF0ZSUyNTIwYSUyNTIwRmlyZXdhbGw

Creates a new Firewall.

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `server_already_added`        | Server added more than one time to resource                   |
| `incompatible_network_type`   | The Network type is incompatible for the given resource       |
| `firewall_resource_not_found` | The resource the Firewall should be attached to was not found |

:information_source: **Note** This endpoint does not require authentication.

```csharp
CreateAFirewallAsync(
    Models.CreateFirewallRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreateFirewallRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/create-firewall-request.md) | Body, Optional | - |


# Response Type

**201**: The `firewall` key contains the Firewall that was just created

[`Task<Models.CreateFirewallResponse>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/create-firewall-response.md)


# Example Usage

```csharp
CreateFirewallRequest body = new CreateFirewallRequest
{
    Name = "Corporate Intranet Protection",
    ApplyTo = new List<ApplyTo>
    {
        new ApplyTo
        {
            Type = Type7Enum.Server,
            Server = new Server2
            {
                Id = 42,
            },
        },
    },
    Labels = ApiHelper.JsonDeserialize<object>("{\"env\":\"dev\"}"),
    Rules = new List<Rule>
    {
        new Rule
        {
            Direction = DirectionEnum.In,
            Protocol = ProtocolEnum.Tcp,
            Description = "Allow port 80",
            Port = "80",
            SourceIps = new List<string>
            {
                "28.239.13.1/32",
                "28.239.14.0/24",
                "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
            },
        },
    },
};

try
{
    CreateFirewallResponse result = await firewallsController.CreateAFirewallAsync(body);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



