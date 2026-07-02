# Uptime Alert Create

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRlVwdGltZSUyRnVwdGltZV9hbGVydF9jcmVhdGU

To create an Uptime alert, send a POST request to `/v2/uptime/checks/$CHECK_ID/alerts` specifying the attributes
in the table below in the JSON body.

```go
UptimeAlertCreate(
    ctx context.Context,
    checkId uuid.UUID,
    body models.Alerts1) (
    models.ApiResponse[models.V2UptimeChecksAlertsResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkId` | `uuid.UUID` | Template, Required | A unique identifier for a check. |
| `body` | [`models.Alerts1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/alerts-1.md) | Body, Required | The ''type'' field dictates the type of alert, and hence what type of value to pass into the threshold property.<br>Type \| Description \| Threshold Value<br>-----\|-------------\|--------------------<br>`latency` \| alerts on the response latency \| milliseconds<br>`down` \| alerts on a target registering as down in any region \| N/A (Not required)<br>`down_global` \| alerts on a target registering as down globally \| N/A (Not required)<br>`ssl_expiry` \| alerts on a SSL certificate expiring within $threshold days \| days |


# Response Type

**201**: The response will be a JSON object with a key called `alert`. The value of this will be an object that contains the standard attributes associated with an uptime alert.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2UptimeChecksAlertsResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-uptime-checks-alerts-response-1.md).


# Example Usage

```go
ctx := context.Background()

checkId := uuid.MustParse("4de7ac8b-495b-4884-9a69-1050c6793cd6")

body := models.Alerts1{
    Comparison:            models.ToPointer(models.Comparison_GreaterThan),
    Name:                  models.ToPointer("Landing page degraded performance"),
    Period:                models.ToPointer(models.Period_Enum2M),
    Threshold:             models.ToPointer(300),
    Type:                  models.ToPointer(models.Type20_Latency),
}

apiResponse, err := uptimeApi.UptimeAlertCreate(ctx, checkId, body)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.V21Clicks401Error:
            log.Fatalln("V21Clicks401ErrorException: ", typedErr)
        default:
            log.Fatalln(err)
    }
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



