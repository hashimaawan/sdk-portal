# Databases Reset Auth

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkRhdGFiYXNlcyUyRmRhdGFiYXNlc19yZXNldF9hdXRo

To reset the password for a database user, send a POST request to
`/v2/databases/$DATABASE_ID/users/$USERNAME/reset_auth`.

For `mysql` databases, the authentication method can be specifying by
including a key in the JSON body called `mysql_settings` with the `auth_plugin`
value specified.

The response will be a JSON object with a `user` key. This will be set to an
object containing the standard database user attributes.

```csharp
DatabasesResetAuthAsync(
    Guid databaseClusterUuid,
    string username,
    Models.V2DatabasesUsersResetAuthRequest body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `databaseClusterUuid` | `Guid` | Template, Required | A unique identifier for a database cluster. |
| `username` | `string` | Template, Required | The name of the database user. |
| `body` | [`V2DatabasesUsersResetAuthRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-databases-users-reset-auth-request.md) | Body, Required | - |


# Response Type

**200**: A JSON object with a key of `user`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.V2DatabasesUsersResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-databases-users-response-1.md).


# Example Usage

```csharp
Guid databaseClusterUuid = new Guid("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30");
string username = "app-01";
V2DatabasesUsersResetAuthRequest body = new V2DatabasesUsersResetAuthRequest
{
    MysqlSettings = new MysqlSettings
    {
        AuthPlugin = AuthPlugin.CachingSha2Password,
    },
};

try
{
    ApiResponse<V2DatabasesUsersResponse1> result = await databasesApi.DatabasesResetAuthAsync(
        databaseClusterUuid,
        username,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
    if (e is V21Clicks401ErrorException)
    {
       // TODO: Handle V21Clicks401ErrorException exception here
    }
}
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/exceptions/v2-1-clicks-401-error.md) |



