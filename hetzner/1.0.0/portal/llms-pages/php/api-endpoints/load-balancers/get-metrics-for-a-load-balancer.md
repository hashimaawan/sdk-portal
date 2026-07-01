# Get Metrics for a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRkdldCUyNTIwTWV0cmljcyUyNTIwZm9yJTI1MjBhJTI1MjBMb2FkQmFsYW5jZXI

You must specify the type of metric to get: `open_connections`, `connections_per_second`, `requests_per_second` or `bandwidth`. You can also specify more than one type by comma separation, e.g. `requests_per_second,bandwidth`.

Depending on the type you will get different time series data:

|Type | Timeseries | Unit | Description |
|---- |------------|------|-------------|
| open_connections | open_connections | number | Open connections |
| connections_per_second | connections_per_second | connections/s | Connections per second |
| requests_per_second | requests_per_second | requests/s | Requests per second |
| bandwidth | bandwidth.in | bytes/s | Ingress bandwidth |
|| bandwidth.out | bytes/s | Egress bandwidth |

Metrics are available for the last 30 days only.

If you do not provide the step argument we will automatically adjust it so that 200 samples are returned.

We limit the number of samples to a maximum of 500 and will adjust the step parameter accordingly.

:information_source: **Note** This endpoint does not require authentication.

```php
function getMetricsForALoadBalancer(
    int $id,
    string $type,
    string $start,
    string $end,
    ?string $step = null
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `type` | [`string(Type41)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-41.md) | Query, Required | Type of metrics to get |
| `start` | `string` | Query, Required | Start of period to get Metrics for (in ISO-8601 format) |
| `end` | `string` | Query, Required | End of period to get Metrics for (in ISO-8601 format) |
| `step` | `?string` | Query, Optional | Resolution of results in seconds |


# Response Type

**200**: The `metrics` key in the reply contains a metrics object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`LoadBalancersMetricsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancers-metrics-response.md).


# Example Usage

```php
$id = 112;

$type = Type41::REQUESTS_PER_SECOND;

$start = 'start4';

$end = 'end8';

$loadBalancersApi = $client->getLoadBalancersApi();
$apiResponse = $loadBalancersApi->getMetricsForALoadBalancer(
    $id,
    $type,
    $start,
    $end
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'LoadBalancersMetricsResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



