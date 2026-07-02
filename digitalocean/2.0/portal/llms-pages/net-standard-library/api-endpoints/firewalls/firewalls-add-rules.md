# Firewalls Add Rules

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRmZpcmV3YWxsc19hZGRfcnVsZXM

To add additional access rules to a firewall, send a POST request to
`/v2/firewalls/$FIREWALL_ID/rules`. The body of the request may include an
inbound_rules and/or outbound_rules attribute containing an array of rules to
be added.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.

```csharp
FirewallsAddRulesAsync(
    Guid firewallId,
    Models.V2FirewallsRulesRequest body = null)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewallId` | `Guid` | Template, Required | A unique ID that can be used to identify and reference a firewall. |
| `body` | [`V2FirewallsRulesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-firewalls-rules-request.md) | Body, Optional | - |


# Response Type

**204**: The action was successful and the response body is empty.

`Task`


# Example Usage

```csharp
Guid firewallId = new Guid("bb4b2611-3d72-467b-8602-280330ecd65c");
V2FirewallsRulesRequest body = new V2FirewallsRulesRequest
{
    InboundRules = new List<InboundRule>
    {
        new InboundRule
        {
            Ports = "3306",
            Protocol = Protocol.Tcp,
            Sources = new Sources
            {
                DropletIds = new List<int>
                {
                    49696269,
                },
            },
        },
    },
    OutboundRules = new List<OutboundRule>
    {
        new OutboundRule
        {
            Ports = "3306",
            Protocol = Protocol.Tcp,
            Destinations = new Destinations
            {
                DropletIds = new List<int>
                {
                    49696269,
                },
            },
        },
    },
};

try
{
    await firewallsApi.FirewallsAddRulesAsync(
        firewallId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
    if (e is V21Clicks401ErrorException)
    {
       // TODO: Handle V21Clicks401ErrorException exception here
    }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |



