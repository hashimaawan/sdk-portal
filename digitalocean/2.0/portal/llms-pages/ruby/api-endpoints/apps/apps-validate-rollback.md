# Apps Validate Rollback

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRkFwcHMlMkZhcHBzX3ZhbGlkYXRlX3JvbGxiYWNr

Check whether an app can be rolled back to a specific deployment. This endpoint can also be used
to check if there are any warnings or validation conditions that will cause the rollback to proceed
under unideal circumstances. For example, if a component must be rebuilt as part of the rollback
causing it to take longer than usual.

```ruby
def apps_validate_rollback(app_id,
                           body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app_id` | `String` | Template, Required | The app ID |
| `body` | [`V2AppsRollbackRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-apps-rollback-request.md) | Body, Required | - |


# Response Type

**200**: A JSON object with the validation results.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`V2AppsRollbackValidateResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-apps-rollback-validate-response.md).


# Example Usage

```ruby
app_id = '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf'

body = V2AppsRollbackRequest.new(
  deployment_id: '3aa4d20e-5527-4c00-b496-601fbd22520a',
  skip_pin: false
)

result = apps_api.apps_validate_rollback(
  app_id,
  body
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
  "error": {
    "code": "incompatible_result",
    "message": "deployment result \"failed\" is unsuitable for rollback"
  },
  "valid": false
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/exceptions/v2-1-clicks-401-error.md) |



