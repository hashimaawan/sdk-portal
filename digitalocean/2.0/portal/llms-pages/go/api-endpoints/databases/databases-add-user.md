# Databases Add User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkRhdGFiYXNlcyUyRmRhdGFiYXNlc19hZGRfdXNlcg

To add a new database user, send a POST request to `/v2/databases/$DATABASE_ID/users`
with the desired username.

Note: User management is not supported for Redis clusters.

When adding a user to a MySQL cluster, additional options can be configured in the
`mysql_settings` object.

The response will be a JSON object with a key called `user`. The value of this will be an
object that contains the standard attributes associated with a database user including
its randomly generated password.

```go
DatabasesAddUser(
    ctx context.Context,
    databaseClusterUuid uuid.UUID,
    body models.User) (
    models.ApiResponse[models.V2DatabasesUsersResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `databaseClusterUuid` | `uuid.UUID` | Template, Required | A unique identifier for a database cluster. |
| `body` | [`models.User`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/user.md) | Body, Required | - |


# Response Type

**201**: A JSON object with a key of `user`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2DatabasesUsersResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-databases-users-response-1.md).


# Example Usage

```go
ctx := context.Background()

databaseClusterUuid := uuid.MustParse("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30")

body := models.User{
    Name:                  "app-01",
}

apiResponse, err := databasesApi.DatabasesAddUser(ctx, databaseClusterUuid, body)
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
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/exceptions/v2-1-clicks-401-error.md) |



