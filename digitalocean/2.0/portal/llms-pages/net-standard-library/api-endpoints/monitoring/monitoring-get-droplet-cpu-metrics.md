# Monitoring Get Droplet Cpu Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRk1vbml0b3JpbmclMkZtb25pdG9yaW5nX2dldF9Ecm9wbGV0Q3B1TWV0cmljcw

To retrieve CPU metrics for a given droplet, send a GET request to `/v2/monitoring/metrics/droplet/cpu`.

```csharp
MonitoringGetDropletCpuMetricsAsync(
    string hostId,
    string start,
    string end)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `hostId` | `string` | Query, Required | The droplet ID. |
| `start` | `string` | Query, Required | Timestamp to start metric window. |
| `end` | `string` | Query, Required | Timestamp to end metric window. |


# Response Type

**200**: The response will be a JSON object with a key called `data` and `status`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.V2MonitoringMetricsDropletBandwidthResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-monitoring-metrics-droplet-bandwidth-response.md).


# Example Usage

```csharp
string hostId = "17209102";
string start = "1620683817";
string end = "1620705417";
try
{
    ApiResponse<V2MonitoringMetricsDropletBandwidthResponse> result = await monitoringApi.MonitoringGetDropletCpuMetricsAsync(
        hostId,
        start,
        end
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


# Example Response *(as JSON)*

```json
{
  "data": {
    "result": [
      {
        "metric": {
          "host_id": "222651441",
          "mode": "idle"
        },
        "values": [
          [
            1635386880,
            "122901.18"
          ],
          [
            1635387000,
            "123020.92"
          ],
          [
            1635387120,
            "123140.8"
          ]
        ]
      },
      {
        "metric": {
          "host_id": "222651441",
          "mode": "iowait"
        },
        "values": [
          [
            1635386880,
            "14.99"
          ],
          [
            1635387000,
            "15.01"
          ],
          [
            1635387120,
            "15.01"
          ]
        ]
      },
      {
        "metric": {
          "host_id": "222651441",
          "mode": "irq"
        },
        "values": [
          [
            1635386880,
            "0"
          ],
          [
            1635387000,
            "0"
          ],
          [
            1635387120,
            "0"
          ]
        ]
      },
      {
        "metric": {
          "host_id": "222651441",
          "mode": "nice"
        },
        "values": [
          [
            1635386880,
            "66.35"
          ],
          [
            1635387000,
            "66.35"
          ],
          [
            1635387120,
            "66.35"
          ]
        ]
      },
      {
        "metric": {
          "host_id": "222651441",
          "mode": "softirq"
        },
        "values": [
          [
            1635386880,
            "2.13"
          ],
          [
            1635387000,
            "2.13"
          ],
          [
            1635387120,
            "2.13"
          ]
        ]
      },
      {
        "metric": {
          "host_id": "222651441",
          "mode": "steal"
        },
        "values": [
          [
            1635386880,
            "7.89"
          ],
          [
            1635387000,
            "7.9"
          ],
          [
            1635387120,
            "7.91"
          ]
        ]
      },
      {
        "metric": {
          "host_id": "222651441",
          "mode": "system"
        },
        "values": [
          [
            1635386880,
            "140.09"
          ],
          [
            1635387000,
            "140.2"
          ],
          [
            1635387120,
            "140.23"
          ]
        ]
      },
      {
        "metric": {
          "host_id": "222651441",
          "mode": "user"
        },
        "values": [
          [
            1635386880,
            "278.57"
          ],
          [
            1635387000,
            "278.65"
          ],
          [
            1635387120,
            "278.69"
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |



