# Monitoring Get Droplet Bandwidth Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRk1vbml0b3JpbmclMkZtb25pdG9yaW5nX2dldF9kcm9wbGV0QmFuZHdpZHRoTWV0cmljcw

To retrieve bandwidth metrics for a given Droplet, send a GET request to `/v2/monitoring/metrics/droplet/bandwidth`. Use the `interface` query parameter to specify if the results should be for the `private` or `public` interface. Use the `direction` query parameter to specify if the results should be for `inbound` or `outbound` traffic.

```python
def monitoring_get_droplet_bandwidth_metrics(self,
                                            host_id,
                                            interface,
                                            direction,
                                            start,
                                            end)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `host_id` | `str` | Query, Required | The droplet ID. |
| `interface` | [`Interface`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/interface.md) | Query, Required | The network interface. |
| `direction` | [`Direction`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/direction.md) | Query, Required | The traffic direction. |
| `start` | `str` | Query, Required | Timestamp to start metric window. |
| `end` | `str` | Query, Required | Timestamp to end metric window. |


# Response Type

**200**: The response will be a JSON object with a key called `data` and `status`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`V2MonitoringMetricsDropletBandwidthResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-monitoring-metrics-droplet-bandwidth-response.md).


# Example Usage

```python
host_id = '17209102'

interface = Interface.PRIVATE

direction = Direction.INBOUND

start = '1620683817'

end = '1620705417'

result = monitoring_api.monitoring_get_droplet_bandwidth_metrics(
    host_id,
    interface,
    direction,
    start,
    end
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |



