# Apps Assign Alert Destinations

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2Fzc2lnbl9hbGVydERlc3RpbmF0aW9ucw

Updates the emails and slack webhook destinations for app alerts. Emails must be associated to a user with access to the app.

```go
AppsAssignAlertDestinations(
    ctx context.Context,
    appId string,
    alertId string,
    body models.V2AppsAlertsDestinationsRequest) (
    models.ApiResponse[models.V2AppsAlertsDestinationsResponse],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appId` | `string` | Template, Required | The app ID |
| `alertId` | `string` | Template, Required | The alert ID |
| `body` | [`models.V2AppsAlertsDestinationsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-apps-alerts-destinations-request.md) | Body, Required | - |


# Response Type

**200**: A JSON object with an `alert` key. This is an object of type `alert`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2AppsAlertsDestinationsResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-apps-alerts-destinations-response.md).


# Example Usage

```go
ctx := context.Background()

appId := "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf"

alertId := "5a624ab5-dd58-4b39-b7dd-8b7c36e8a91d"

body := models.V2AppsAlertsDestinationsRequest{
    Emails:                []string{
        "sammy@digitalocean.com",
    },
}

apiResponse, err := appsApi.AppsAssignAlertDestinations(ctx, appId, alertId, body)
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
  "alert": {
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
  }
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



