# Get Prometheus Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0ZSUyRk1ldHJpY3MlMkZHZXRQcm9tZXRoZXVzTWV0cmljcw

See Prometheus documentation for a complete data model.

:information_source: **Note** This endpoint does not require authentication.

```go
GetPrometheusMetrics(
    ctx context.Context) (
    models.ApiResponse[string],
    error)
```


# Response Type

**200**: Successfully returned Prometheus metrics

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type string.


# Example Usage

```go
ctx := context.Background()

apiResponse, err := metricsApi.GetPrometheusMetrics(ctx)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```



