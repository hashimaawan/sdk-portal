# Monitoring Get Droplet Filesystem Size Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRk1vbml0b3JpbmclMkZtb25pdG9yaW5nX2dldF9kcm9wbGV0RmlsZXN5c3RlbVNpemVNZXRyaWNz

To retrieve filesystem size metrics for a given droplet, send a GET request to `/v2/monitoring/metrics/droplet/filesystem_size`.

```ruby
def monitoring_get_droplet_filesystem_size_metrics(host_id,
                                                   start,
                                                   mend)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `host_id` | `String` | Query, Required | The droplet ID. |
| `start` | `String` | Query, Required | Timestamp to start metric window. |
| `mend` | `String` | Query, Required | Timestamp to end metric window. |


# Response Type

**200**: The response will be a JSON object with a key called `data` and `status`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`V2MonitoringMetricsDropletBandwidthResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-monitoring-metrics-droplet-bandwidth-response.md).


# Example Usage

```ruby
host_id = '17209102'

start = '1620683817'

mend = '1620705417'

result = monitoring_api.monitoring_get_droplet_filesystem_size_metrics(
  host_id,
  start,
  mend
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Example Response *(as JSON)*

```json
{
  "data": {
    "result": [
      {
        "metric": {
          "device": "/dev/vda1",
          "fstype": "ext4",
          "host_id": "222651441",
          "mountpoint": "/"
        },
        "values": [
          [
            1635386880,
            "25832407040"
          ],
          [
            1635387000,
            "25832407040"
          ],
          [
            1635387120,
            "25832407040"
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |



