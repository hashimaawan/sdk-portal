# Uptime Check Update

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRlVwdGltZSUyRnVwdGltZV9jaGVja191cGRhdGU

To update the settings of an Uptime check, send a PUT request to `/v2/uptime/checks/$CHECK_ID`.

```go
UptimeCheckUpdate(
    ctx context.Context,
    checkId uuid.UUID,
    body models.V2UptimeChecksRequest) (
    models.ApiResponse[models.V2UptimeChecksResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkId` | `uuid.UUID` | Template, Required | A unique identifier for a check. |
| `body` | [`models.V2UptimeChecksRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-uptime-checks-request.md) | Body, Required | - |


# Response Type

**200**: The response will be a JSON object with a key called `check`. The value of this will be an object that contains the standard attributes associated with an uptime check.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2UptimeChecksResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-uptime-checks-response-1.md).


# Example Usage

```go
ctx := context.Background()

checkId := uuid.MustParse("4de7ac8b-495b-4884-9a69-1050c6793cd6")

body := models.V2UptimeChecksRequest{
    Enabled:               models.ToPointer(true),
    Name:                  models.ToPointer("Landing page check"),
    Regions:               []models.Region8{
        models.Region8_UsEast,
        models.Region8_EuWest,
    },
    Target:                models.ToPointer("https://www.landingpage.com"),
    Type:                  models.ToPointer(models.Type19_Https),
}

apiResponse, err := uptimeApi.UptimeCheckUpdate(ctx, checkId, body)
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



