# Uptime Alert Update

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRlVwdGltZSUyRnVwdGltZV9hbGVydF91cGRhdGU

To update the settings of an Uptime alert, send a PUT request to `/v2/uptime/checks/$CHECK_ID/alerts/$ALERT_ID`.

```ts
async uptimeAlertUpdate(
  checkId: string,
  alertId: string,
  body: V2UptimeChecksAlertsRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2UptimeChecksAlertsResponse1>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkId` | `string` | Template, Required | A unique identifier for a check. |
| `alertId` | `string` | Template, Required | A unique identifier for an alert. |
| `body` | [`V2UptimeChecksAlertsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-uptime-checks-alerts-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The response will be a JSON object with a key called `alert`. The value of this will be an object that contains the standard attributes associated with an uptime alert.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2UptimeChecksAlertsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-uptime-checks-alerts-response-1.md).


# Example Usage

```ts
const checkId = '4de7ac8b-495b-4884-9a69-1050c6793cd6';

const alertId = '17f0f0ae-b7e5-4ef6-86e3-aa569db58284';

const body: V2UptimeChecksAlertsRequest = {
  comparison: Comparison.GreaterThan,
  name: 'Landing page degraded performance',
  period: Period.Enum2M,
  threshold: 300,
  type: Type20.Latency,
};

try {
  const response = await uptimeApi.uptimeAlertUpdate(
    checkId,
    alertId,
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



