# Monitoring Update Alert Policy

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRk1vbml0b3JpbmclMkZtb25pdG9yaW5nX3VwZGF0ZV9hbGVydFBvbGljeQ

To update en existing policy, send a PUT request to `v2/monitoring/alerts/{alert_uuid}`.

```ts
async monitoringUpdateAlertPolicy(
  alertUuid: string,
  body: V2MonitoringAlertsRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2MonitoringAlertsResponse1>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alertUuid` | `string` | Template, Required | A unique identifier for an alert policy. |
| `body` | [`V2MonitoringAlertsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-monitoring-alerts-request.md) | Body, Required | The `type` field dictates what type of entity that the alert policy applies to and hence what type of entity is passed in the `entities` array. If both the `tags` array and `entities` array are empty the alert policy applies to all entities of the relevant type that are owned by the user account. Otherwise the following table shows the valid entity types for each type of alert policy:<br><br>Type \| Description \| Valid Entity Type<br>-----\|-------------\|--------------------<br>`v1/insights/droplet/memory_utilization_percent` \| alert on the percent of memory utilization \| Droplet ID<br>`v1/insights/droplet/disk_read` \| alert on the rate of disk read I/O in MBps \| Droplet ID<br>`v1/insights/droplet/load_5` \| alert on the 5 minute load average \| Droplet ID<br>`v1/insights/droplet/load_15` \| alert on the 15 minute load average \| Droplet ID<br>`v1/insights/droplet/disk_utilization_percent` \| alert on the percent of disk utilization \| Droplet ID<br>`v1/insights/droplet/cpu` \| alert on the percent of CPU utilization \| Droplet ID<br>`v1/insights/droplet/disk_write` \| alert on the rate of disk write I/O in MBps \| Droplet ID<br>`v1/insights/droplet/public_outbound_bandwidth` \| alert on the rate of public outbound bandwidth in Mbps \| Droplet ID<br>`v1/insights/droplet/public_inbound_bandwidth` \| alert on the rate of public inbound bandwidth in Mbps \| Droplet ID<br>`v1/insights/droplet/private_outbound_bandwidth` \| alert on the rate of private outbound bandwidth in Mbps \| Droplet ID<br>`v1/insights/droplet/private_inbound_bandwidth` \| alert on the rate of private inbound bandwidth in Mbps \| Droplet ID<br>`v1/insights/droplet/load_1` \| alert on the 1 minute load average \| Droplet ID<br>`v1/insights/lbaas/avg_cpu_utilization_percent`\|alert on the percent of CPU utilization\|load balancer ID<br>`v1/insights/lbaas/connection_utilization_percent`\|alert on the percent of connection utilization\|load balancer ID<br>`v1/insights/lbaas/droplet_health`\|alert on Droplet health status changes\|load balancer ID<br>`v1/insights/lbaas/tls_connections_per_second_utilization_percent`\|alert on the percent of TLS connections per second utilization\|load balancer ID<br>`v1/insights/lbaas/increase_in_http_error_rate_percentage_5xx`\|alert on the percent increase of 5xx level http errors over 5m\|load balancer ID<br>`v1/insights/lbaas/increase_in_http_error_rate_percentage_4xx`\|alert on the percent increase of 4xx level http errors over 5m\|load balancer ID<br>`v1/insights/lbaas/increase_in_http_error_rate_count_5xx`\|alert on the count of 5xx level http errors over 5m\|load balancer ID<br>`v1/insights/lbaas/increase_in_http_error_rate_count_4xx`\|alert on the count of 4xx level http errors over 5m\|load balancer ID<br>`v1/insights/lbaas/high_http_request_response_time`\|alert on high average http response time\|load balancer ID<br>`v1/insights/lbaas/high_http_request_response_time_50p`\|alert on high 50th percentile http response time\|load balancer ID<br>`v1/insights/lbaas/high_http_request_response_time_95p`\|alert on high 95th percentile http response time\|load balancer ID<br>`v1/insights/lbaas/high_http_request_response_time_99p`\|alert on high 99th percentile http response time\|load balancer ID<br>`v1/dbaas/alerts/load_15_alerts` \| alert on 15 minute load average across the database cluster \| database cluster UUID<br>`v1/dbaas/alerts/memory_utilization_alerts` \| alert on the percent memory utilization average across the database cluster \| database cluster UUID<br>`v1/dbaas/alerts/disk_utilization_alerts` \| alert on the percent disk utilization average across the database cluster \| database cluster UUID<br>`v1/dbaas/alerts/cpu_alerts` \| alert on the percent CPU usage average across the database cluster \| database cluster UUID |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: An alert policy.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2MonitoringAlertsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-monitoring-alerts-response-1.md).


# Example Usage

```ts
const alertUuid = '4de7ac8b-495b-4884-9a69-1050c6793cd6';

const body: V2MonitoringAlertsRequest = {
  alerts: {
    email: [
      'bob@exmaple.com'
    ],
    slack: [
      {
        channel: 'Production Alerts',
        url: 'https://hooks.slack.com/services/T1234567/AAAAAAAA/ZZZZZZ',
      }
    ],
  },
  compare: Compare.GreaterThan,
  description: 'CPU Alert',
  enabled: true,
  entities: [
    '192018292'
  ],
  tags: [
    'droplet_tag'
  ],
  type: Type17.EnumV1Insightsdropletcpu,
  value: 80,
  window: Window1.Enum5M,
};

try {
  const response = await monitoringApi.monitoringUpdateAlertPolicy(
    alertUuid,
    body
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


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |



