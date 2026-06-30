# Get Prometheus Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0ZSUyRk1ldHJpY3MlMkZHZXRQcm9tZXRoZXVzTWV0cmljcw

See Prometheus documentation for a complete data model.

:information_source: **Note** This endpoint does not require authentication.

```php
function getPrometheusMetrics(): ApiResponse
```


# Response Type

**200**: Successfully returned Prometheus metrics

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type `string`.


# Example Usage

```php
$metricsApi = $client->getMetricsApi();
$apiResponse = $metricsApi->getPrometheusMetrics();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'string:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



