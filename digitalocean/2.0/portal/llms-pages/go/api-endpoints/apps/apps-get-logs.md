# Apps Get Logs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2dldF9sb2dz

Retrieve the logs of a past, in-progress, or active deployment. The response will include links to either real-time logs of an in-progress or active deployment or archived logs of a past deployment.

```go
AppsGetLogs(
    ctx context.Context,
    appId string,
    deploymentId string,
    componentName string,
    mType models.Type3,
    follow *bool,
    podConnectionTimeout *string) (
    models.ApiResponse[models.V2AppsComponentsLogsResponse],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appId` | `string` | Template, Required | The app ID |
| `deploymentId` | `string` | Template, Required | The deployment ID |
| `componentName` | `string` | Template, Required | An optional component name. If set, logs will be limited to this component only. |
| `mType` | [`models.Type3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/type-3.md) | Query, Required | The type of logs to retrieve<br><br>- BUILD: Build-time logs<br>- DEPLOY: Deploy-time logs<br>- RUN: Live run-time logs |
| `follow` | `*bool` | Query, Optional | Whether the logs should follow live updates. |
| `podConnectionTimeout` | `*string` | Query, Optional | An optional time duration to wait if the underlying component instance is not immediately available. Default: `3m`. |


# Response Type

**200**: A JSON object with urls that point to archived logs

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2AppsComponentsLogsResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-apps-components-logs-response.md).


# Example Usage

```go
ctx := context.Background()

appId := "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf"

deploymentId := "3aa4d20e-5527-4c00-b496-601fbd22520a"

componentName := "component"

mType := models.Type3_Build

follow := true

podConnectionTimeout := "3m"

apiResponse, err := appsApi.AppsGetLogs(ctx, appId, deploymentId, componentName, mType, &follow, &podConnectionTimeout)
if err != nil {
    switch typedErr := err.(type) {
        case *errors.V21Clicks401Error:
            log.Fatalln("V21Clicks401ErrorException: ", typedErr)
        default:
            log.Fatalln(err)
    }
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



