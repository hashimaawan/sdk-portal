# Monitoring Get Droplet Bandwidth Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRk1vbml0b3JpbmclMkZtb25pdG9yaW5nX2dldF9kcm9wbGV0QmFuZHdpZHRoTWV0cmljcw

To retrieve bandwidth metrics for a given Droplet, send a GET request to `/v2/monitoring/metrics/droplet/bandwidth`. Use the `interface` query parameter to specify if the results should be for the `private` or `public` interface. Use the `direction` query parameter to specify if the results should be for `inbound` or `outbound` traffic.

```ts
async monitoringGetDropletBandwidthMetrics(
  hostId: string,
  mInterface: Interface,
  direction: Direction,
  start: string,
  end: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2MonitoringMetricsDropletBandwidthResponse>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `hostId` | `string` | Query, Required | The droplet ID. |
| `mInterface` | [`Interface`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/interface.md) | Query, Required | The network interface. |
| `direction` | [`Direction`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/direction.md) | Query, Required | The traffic direction. |
| `start` | `string` | Query, Required | Timestamp to start metric window. |
| `end` | `string` | Query, Required | Timestamp to end metric window. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The response will be a JSON object with a key called `data` and `status`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2MonitoringMetricsDropletBandwidthResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-monitoring-metrics-droplet-bandwidth-response.md).


# Example Usage

```ts
const hostId = '17209102';

const mInterface = Interface.Private;

const direction = Direction.Inbound;

const start = '1620683817';

const end = '1620705417';

try {
  const response = await monitoringApi.monitoringGetDropletBandwidthMetrics(
    hostId,
    mInterface,
    direction,
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
    if (error instanceof V21Clicks401Error) {
      console.log(error.result);
    }
  }
}
```


# Example Response *(as JSON)*

```json
{
  "data": {
    "result": [
      {
        "metric": {
          "direction": "inbound",
          "host_id": "222651441",
          "interface": "private"
        },
        "values": [
          [
            1634052360,
            "0.016600450090265357"
          ],
          [
            1634052480,
            "0.015085955677299055"
          ],
          [
            1634052600,
            "0.014941163855322308"
          ],
          [
            1634052720,
            "0.016214285714285712"
          ]
        ]
      }
    ],
    "resultType": "matrix"
  },
  "status": "success"
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |



