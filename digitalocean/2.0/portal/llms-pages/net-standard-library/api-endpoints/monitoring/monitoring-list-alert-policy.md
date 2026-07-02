# Monitoring List Alert Policy

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRk1vbml0b3JpbmclMkZtb25pdG9yaW5nX2xpc3RfYWxlcnRQb2xpY3k

Returns all alert policies that are configured for the given account. To List all alert policies, send a GET request to `/v2/monitoring/alerts`.

```csharp
MonitoringListAlertPolicyAsync(
    int? perPage = 20,
    int? page = 1)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `perPage` | `int?` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `page` | `int?` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |


# Response Type

**200**: A list of alert policies.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.V2MonitoringAlertsResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-monitoring-alerts-response.md).


# Example Usage

```csharp
int? perPage = 2;
int? page = 1;
try
{
    ApiResponse<V2MonitoringAlertsResponse> result = await monitoringApi.MonitoringListAlertPolicyAsync(
        perPage,
        page
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
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |



