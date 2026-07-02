# Apps Get Logs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX2dldF9sb2dz

Retrieve the logs of a past, in-progress, or active deployment. The response will include links to either real-time logs of an in-progress or active deployment or archived logs of a past deployment.

```python
def apps_get_logs(self,
                 app_id,
                 deployment_id,
                 component_name,
                 mtype,
                 follow=None,
                 pod_connection_timeout=None)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app_id` | `str` | Template, Required | The app ID |
| `deployment_id` | `str` | Template, Required | The deployment ID |
| `component_name` | `str` | Template, Required | An optional component name. If set, logs will be limited to this component only. |
| `mtype` | [`Type3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/type-3.md) | Query, Required | The type of logs to retrieve<br><br>- BUILD: Build-time logs<br>- DEPLOY: Deploy-time logs<br>- RUN: Live run-time logs |
| `follow` | `bool` | Query, Optional | Whether the logs should follow live updates. |
| `pod_connection_timeout` | `str` | Query, Optional | An optional time duration to wait if the underlying component instance is not immediately available. Default: `3m`. |


# Response Type

**200**: A JSON object with urls that point to archived logs

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`V2AppsComponentsLogsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-apps-components-logs-response.md).


# Example Usage

```python
app_id = '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf'

deployment_id = '3aa4d20e-5527-4c00-b496-601fbd22520a'

component_name = 'component'

mtype = Type3.BUILD

follow = True

pod_connection_timeout = '3m'

result = apps_api.apps_get_logs(
    app_id,
    deployment_id,
    component_name,
    mtype,
    follow=follow,
    pod_connection_timeout=pod_connection_timeout
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/exceptions/v2-1-clicks-401-error.md) |



