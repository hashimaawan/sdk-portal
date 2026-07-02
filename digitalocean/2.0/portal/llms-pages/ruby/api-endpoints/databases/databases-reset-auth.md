# Databases Reset Auth

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0ZSUyRkRhdGFiYXNlcyUyRmRhdGFiYXNlc19yZXNldF9hdXRo

To reset the password for a database user, send a POST request to
`/v2/databases/$DATABASE_ID/users/$USERNAME/reset_auth`.

For `mysql` databases, the authentication method can be specifying by
including a key in the JSON body called `mysql_settings` with the `auth_plugin`
value specified.

The response will be a JSON object with a `user` key. This will be set to an
object containing the standard database user attributes.

```ruby
def databases_reset_auth(database_cluster_uuid,
                         username,
                         body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database_cluster_uuid` | `UUID \| String` | Template, Required | A unique identifier for a database cluster. |
| `username` | `String` | Template, Required | The name of the database user. |
| `body` | [`V2DatabasesUsersResetAuthRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-databases-users-reset-auth-request.md) | Body, Required | - |


# Response Type

**200**: A JSON object with a key of `user`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`V2DatabasesUsersResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-databases-users-response-1.md).


# Example Usage

```ruby
database_cluster_uuid = '9cc10173-e9ea-4176-9dbc-a4cee4c4ff30'

username = 'app-01'

body = V2DatabasesUsersResetAuthRequest.new(
  mysql_settings: MysqlSettings.new(
    auth_plugin: AuthPlugin::CACHING_SHA2_PASSWORD
  )
)

result = databases_api.databases_reset_auth(
  database_cluster_uuid,
  username,
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
  "user": {
    "name": "app-01",
    "password": "jge5lfxtzhx42iff",
    "role": "normal"
  }
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



