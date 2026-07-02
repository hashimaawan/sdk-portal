# Uptime Alert Create

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlVwdGltZSUyRnVwdGltZV9hbGVydF9jcmVhdGU

To create an Uptime alert, send a POST request to `/v2/uptime/checks/$CHECK_ID/alerts` specifying the attributes
in the table below in the JSON body.

```csharp
UptimeAlertCreateAsync(
    Guid checkId,
    Models.Alerts1 body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkId` | `Guid` | Template, Required | A unique identifier for a check. |
| `body` | [`Alerts1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/alerts-1.md) | Body, Required | The ''type'' field dictates the type of alert, and hence what type of value to pass into the threshold property.<br>Type \| Description \| Threshold Value<br>-----\|-------------\|--------------------<br>`latency` \| alerts on the response latency \| milliseconds<br>`down` \| alerts on a target registering as down in any region \| N/A (Not required)<br>`down_global` \| alerts on a target registering as down globally \| N/A (Not required)<br>`ssl_expiry` \| alerts on a SSL certificate expiring within $threshold days \| days |


# Response Type

**201**: The response will be a JSON object with a key called `alert`. The value of this will be an object that contains the standard attributes associated with an uptime alert.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.V2UptimeChecksAlertsResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-uptime-checks-alerts-response-1.md).


# Example Usage

```csharp
Guid checkId = new Guid("4de7ac8b-495b-4884-9a69-1050c6793cd6");
Alerts1 body = new Alerts1
{
    Comparison = Comparison.GreaterThan,
    Name = "Landing page degraded performance",
    Period = Period.Enum2M,
    Threshold = 300,
    Type = Type20.Latency,
};

try
{
    ApiResponse<V2UptimeChecksAlertsResponse1> result = await uptimeApi.UptimeAlertCreateAsync(
        checkId,
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



