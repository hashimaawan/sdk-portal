# Apps Get Logs Aggregate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2dldF9sb2dzX2FnZ3JlZ2F0ZQ

Retrieve the logs of a past, in-progress, or active deployment. If a component name is specified, the logs will be limited to only that component. The response will include links to either real-time logs of an in-progress or active deployment or archived logs of a past deployment.

```java
CompletableFuture<ApiResponse<V2AppsComponentsLogsResponse>> appsGetLogsAggregateAsync(
    final String appId,
    final String deploymentId,
    final Type3 type,
    final Boolean follow,
    final String podConnectionTimeout)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appId` | `String` | Template, Required | The app ID |
| `deploymentId` | `String` | Template, Required | The deployment ID |
| `type` | [`Type3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-3.md) | Query, Required | The type of logs to retrieve<br><br>- BUILD: Build-time logs<br>- DEPLOY: Deploy-time logs<br>- RUN: Live run-time logs |
| `follow` | `Boolean` | Query, Optional | Whether the logs should follow live updates. |
| `podConnectionTimeout` | `String` | Query, Optional | An optional time duration to wait if the underlying component instance is not immediately available. Default: `3m`. |


# Response Type

**200**: A JSON object with urls that point to archived logs

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`V2AppsComponentsLogsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-apps-components-logs-response.md).


# Example Usage

```java
String appId = "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf";
String deploymentId = "3aa4d20e-5527-4c00-b496-601fbd22520a";
Type3 type = Type3.BUILD;
Boolean follow = true;
String podConnectionTimeout = "3m";

appsApi.appsGetLogsAggregateAsync(appId, deploymentId, type, follow, podConnectionTimeout).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof V21Clicks401ErrorException) {
        V21Clicks401ErrorException v21Clicks401ErrorException = (V21Clicks401ErrorException) cause;
        v21Clicks401ErrorException.printStackTrace();
    } else {
        // fallback for unexpected errors
        exception.printStackTrace();
    }

    return null;
});
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



