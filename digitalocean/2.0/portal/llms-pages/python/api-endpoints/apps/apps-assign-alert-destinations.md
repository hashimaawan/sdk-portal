# Apps Assign Alert Destinations

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2Fzc2lnbl9hbGVydERlc3RpbmF0aW9ucw

Updates the emails and slack webhook destinations for app alerts. Emails must be associated to a user with access to the app.

```python
def apps_assign_alert_destinations(self,
                                  app_id,
                                  alert_id,
                                  body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app_id` | `str` | Template, Required | The app ID |
| `alert_id` | `str` | Template, Required | The alert ID |
| `body` | [`V2AppsAlertsDestinationsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-apps-alerts-destinations-request.md) | Body, Required | - |


# Response Type

**200**: A JSON object with an `alert` key. This is an object of type `alert`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`V2AppsAlertsDestinationsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-apps-alerts-destinations-response.md).


# Example Usage

```python
app_id = '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf'

alert_id = '5a624ab5-dd58-4b39-b7dd-8b7c36e8a91d'

body = V2AppsAlertsDestinationsRequest(
    emails=[
        'sammy@digitalocean.com'
    ]
)

result = apps_api.apps_assign_alert_destinations(
    app_id,
    alert_id,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |



