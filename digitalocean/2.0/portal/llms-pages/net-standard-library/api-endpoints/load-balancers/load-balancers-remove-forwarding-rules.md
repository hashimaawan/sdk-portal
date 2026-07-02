# Load Balancers Remove Forwarding Rules

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRmxvYWRCYWxhbmNlcnNfcmVtb3ZlX2ZvcndhcmRpbmdSdWxlcw

To remove forwarding rules from a load balancer instance, send a DELETE
request to `/v2/load_balancers/$LOAD_BALANCER_ID/forwarding_rules`. In the
body of the request, there should be a `forwarding_rules` attribute containing
an array of rules to be removed.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.

```csharp
LoadBalancersRemoveForwardingRulesAsync(
    string lbId,
    Models.V2LoadBalancersForwardingRulesRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `lbId` | `string` | Template, Required | A unique identifier for a load balancer. |
| `body` | [`V2LoadBalancersForwardingRulesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-load-balancers-forwarding-rules-request.md) | Body, Required | - |


# Response Type

**204**: The action was successful and the response body is empty.

`Task`


# Example Usage

```csharp
string lbId = "4de7ac8b-495b-4884-9a69-1050c6793cd6";
V2LoadBalancersForwardingRulesRequest body = new V2LoadBalancersForwardingRulesRequest
{
    ForwardingRules = new List<ForwardingRule>
    {
        new ForwardingRule
        {
            EntryPort = 443,
            EntryProtocol = EntryProtocol.Https,
            TargetPort = 80,
            TargetProtocol = TargetProtocol.Http,
            CertificateId = "892071a0-bb95-49bc-8021-3afd67a210bf",
            TlsPassthrough = false,
        },
    },
};

try
{
    await loadBalancersApi.LoadBalancersRemoveForwardingRulesAsync(
        lbId,
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |



