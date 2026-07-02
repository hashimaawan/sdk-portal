# Apps List Alerts

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2xpc3RfYWxlcnRz

List alerts associated to the app and any components. This includes configuration information about the alerts including emails, slack webhooks, and triggering events or conditions.

```ts
async appsListAlerts(
  appId: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2AppsAlertsResponse>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appId` | `string` | Template, Required | The app ID |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: A JSON object with a `alerts` key. This is list of object `alerts`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2AppsAlertsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-apps-alerts-response.md).


# Example Usage

```ts
const appId = '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf';

try {
  const response = await appsApi.appsListAlerts(appId);

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
  "alerts": [
    {
      "emails": [
        "sammy@digitalocean.com"
      ],
      "id": "e552e1f9-c1b0-4e6d-8777-ad6f27767306",
      "phase": "ACTIVE",
      "progress": {
        "steps": [
          {
            "ended_at": "2020-07-28T18:00:00Z",
            "name": "alert-configure-insight-alert",
            "started_at": "2020-07-28T18:00:00Z",
            "status": "SUCCESS"
          }
        ]
      },
      "spec": {
        "rule": "DEPLOYMENT_FAILED"
      }
    },
    {
      "emails": [
        "sammy@digitalocean.com"
      ],
      "id": "b58cc9d4-0702-4ffd-ab45-4c2a8d979527",
      "phase": "ACTIVE",
      "progress": {
        "steps": [
          {
            "ended_at": "2020-07-28T18:00:00Z",
            "name": "alert-configure-insight-alert",
            "started_at": "2020-07-28T18:00:00Z",
            "status": "SUCCESS"
          }
        ]
      },
      "spec": {
        "operator": "GREATER_THAN",
        "rule": "CPU_UTILIZATION",
        "value": 85,
        "window": "FIVE_MINUTES"
      }
    }
  ]
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



