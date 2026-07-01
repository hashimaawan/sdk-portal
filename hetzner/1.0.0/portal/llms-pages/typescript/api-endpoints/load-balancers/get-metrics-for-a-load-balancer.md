# Get Metrics for a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRkdldCUyNTIwTWV0cmljcyUyNTIwZm9yJTI1MjBhJTI1MjBMb2FkQmFsYW5jZXI

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

```ts
async getMetricsForALoadBalancer(
  id: number,
  type: Type41,
  start: string,
  end: string,
  step?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<LoadBalancersMetricsResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Template, Required | ID of the Load Balancer |
| `type` | [`Type41`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-41.md) | Query, Required | Type of metrics to get |
| `start` | `string` | Query, Required | Start of period to get Metrics for (in ISO-8601 format) |
| `end` | `string` | Query, Required | End of period to get Metrics for (in ISO-8601 format) |
| `step` | `string \| undefined` | Query, Optional | Resolution of results in seconds |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The `metrics` key in the reply contains a metrics object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`LoadBalancersMetricsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/load-balancers-metrics-response.md).


# Example Usage

```ts
const id = 112;

const type = Type41.RequestsPerSecond;

const start = 'start4';

const end = 'end8';

try {
  const response = await loadBalancersApi.getMetricsForALoadBalancer(
    id,
    type,
    start,
    end
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```



