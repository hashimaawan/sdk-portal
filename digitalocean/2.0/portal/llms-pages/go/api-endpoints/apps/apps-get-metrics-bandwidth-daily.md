# Apps Get Metrics Bandwidth Daily

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2dldF9tZXRyaWNzX2JhbmR3aWR0aF9kYWlseQ

Retrieve daily bandwidth usage metrics for a single app.

```go
AppsGetMetricsBandwidthDaily(
    ctx context.Context,
    appId string,
    date *time.Time) (
    models.ApiResponse[models.V2AppsMetricsBandwidthDailyResponse],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appId` | `string` | Template, Required | The app ID |
| `date` | `*time.Time` | Query, Optional | Optional day to query. Only the date component of the timestamp will be considered. Default: yesterday. |


# Response Type

**200**: A JSON object with a `app_bandwidth_usage` key

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2AppsMetricsBandwidthDailyResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-apps-metrics-bandwidth-daily-response.md).


# Example Usage

```go
ctx := context.Background()

appId := "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf"

date := parseTime(time.RFC3339, "2023-01-17T00:00:00Z", func(err error) { log.Fatalln(err) })

apiResponse, err := appsApi.AppsGetMetricsBandwidthDaily(ctx, appId, &date)
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


# Example Response *(as JSON)*

```json
{
  "app_bandwidth_usage": [
    {
      "app_id": "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
      "bandwidth_bytes": "513668"
    }
  ],
  "date": "2023-01-17T00:00:00Z"
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



