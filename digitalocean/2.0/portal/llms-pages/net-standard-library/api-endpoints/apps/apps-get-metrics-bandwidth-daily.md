# Apps Get Metrics Bandwidth Daily

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2dldF9tZXRyaWNzX2JhbmR3aWR0aF9kYWlseQ

Retrieve daily bandwidth usage metrics for a single app.

```csharp
AppsGetMetricsBandwidthDailyAsync(
    string appId,
    DateTime? date = null)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appId` | `string` | Template, Required | The app ID |
| `date` | `DateTime?` | Query, Optional | Optional day to query. Only the date component of the timestamp will be considered. Default: yesterday. |


# Response Type

**200**: A JSON object with a `app_bandwidth_usage` key

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.V2AppsMetricsBandwidthDailyResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-apps-metrics-bandwidth-daily-response.md).


# Example Usage

```csharp
string appId = "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf";
DateTime? date = DateTime.ParseExact("2023-01-17T00:00:00Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind);
try
{
    ApiResponse<V2AppsMetricsBandwidthDailyResponse> result = await appsApi.AppsGetMetricsBandwidthDailyAsync(
        appId,
        date
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |



