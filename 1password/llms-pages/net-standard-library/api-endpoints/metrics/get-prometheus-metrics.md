# Get Prometheus Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0ZSUyRk1ldHJpY3MlMkZHZXRQcm9tZXRoZXVzTWV0cmljcw

See Prometheus documentation for a complete data model.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetPrometheusMetricsAsync()
```


# Response Type

**200**: Successfully returned Prometheus metrics

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type string.


# Example Usage

```csharp
try
{
    ApiResponse<string> result = await metricsApi.GetPrometheusMetricsAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



