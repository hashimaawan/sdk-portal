# Apps Get Logs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2dldF9sb2dz

Retrieve the logs of a past, in-progress, or active deployment. The response will include links to either real-time logs of an in-progress or active deployment or archived logs of a past deployment.

```ts
async appsGetLogs(
  appId: string,
  deploymentId: string,
  componentName: string,
  type: Type3,
  follow?: boolean,
  podConnectionTimeout?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2AppsComponentsLogsResponse>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appId` | `string` | Template, Required | The app ID |
| `deploymentId` | `string` | Template, Required | The deployment ID |
| `componentName` | `string` | Template, Required | An optional component name. If set, logs will be limited to this component only. |
| `type` | [`Type3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/type-3.md) | Query, Required | The type of logs to retrieve<br><br>- BUILD: Build-time logs<br>- DEPLOY: Deploy-time logs<br>- RUN: Live run-time logs |
| `follow` | `boolean \| undefined` | Query, Optional | Whether the logs should follow live updates. |
| `podConnectionTimeout` | `string \| undefined` | Query, Optional | An optional time duration to wait if the underlying component instance is not immediately available. Default: `3m`. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: A JSON object with urls that point to archived logs

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2AppsComponentsLogsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-apps-components-logs-response.md).


# Example Usage

```ts
const appId = '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf';

const deploymentId = '3aa4d20e-5527-4c00-b496-601fbd22520a';

const componentName = 'component';

const type = Type3.Build;

const follow = true;

const podConnectionTimeout = '3m';

try {
  const response = await appsApi.appsGetLogs(
    appId,
    deploymentId,
    componentName,
    type,
    follow,
    podConnectionTimeout
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
  "historic_logs": [
    "https://logs-example/archive/build.log"
  ],
  "live_url": "https://logs-example/build.log",
  "url": "https://logs/build.log"
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



