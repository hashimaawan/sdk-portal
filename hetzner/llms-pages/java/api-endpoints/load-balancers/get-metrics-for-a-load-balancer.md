# Get Metrics for a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRkdldCUyNTIwTWV0cmljcyUyNTIwZm9yJTI1MjBhJTI1MjBMb2FkQmFsYW5jZXI

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

```java
CompletableFuture<LoadBalancersMetricsResponse> getMetricsForALoadBalancerAsync(
    final int id,
    final Type41Enum type,
    final String start,
    final String end,
    final String step)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `type` | [`Type41Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/type-41.md) | Query, Required | Type of metrics to get |
| `start` | `String` | Query, Required | Start of period to get Metrics for (in ISO-8601 format) |
| `end` | `String` | Query, Required | End of period to get Metrics for (in ISO-8601 format) |
| `step` | `String` | Query, Optional | Resolution of results in seconds |


# Response Type

**200**: The `metrics` key in the reply contains a metrics object with this structure

[`LoadBalancersMetricsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/load-balancers-metrics-response.md)


# Example Usage

```java
int id = 112;
Type41Enum type = Type41Enum.REQUESTS_PER_SECOND;
String start = "start4";
String end = "end8";

loadBalancersController.getMetricsForALoadBalancerAsync(id, type, start, end, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```



