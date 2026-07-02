# Apps List Metrics Bandwidth Daily

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2xpc3RfbWV0cmljc19iYW5kd2lkdGhfZGFpbHk

Retrieve daily bandwidth usage metrics for multiple apps.

```ruby
def apps_list_metrics_bandwidth_daily(body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V2AppsMetricsBandwidthDailyRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-apps-metrics-bandwidth-daily-request.md) | Body, Required | - |


# Response Type

**200**: A JSON object with a `app_bandwidth_usage` key

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`V2AppsMetricsBandwidthDailyResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-apps-metrics-bandwidth-daily-response.md).


# Example Usage

```ruby
body = V2AppsMetricsBandwidthDailyRequest.new(
  app_ids: [
    '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
    'c2a93513-8d9b-4223-9d61-5e7272c81cf5'
  ],
  date: DateTimeHelper.from_rfc3339('2023-01-17T00:00:00Z')
)

result = apps_api.apps_list_metrics_bandwidth_daily(body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Example Response *(as JSON)*

```json
{
  "app_bandwidth_usage": [
    {
      "app_id": "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
      "bandwidth_bytes": "513668"
    },
    {
      "app_id": "c2a93513-8d9b-4223-9d61-5e7272c81cf5",
      "bandwidth_bytes": "254847"
    }
  ],
  "date": "2023-01-17T00:00:00Z"
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |



