# Databases Get Cluster

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0ZSUyRkRhdGFiYXNlcyUyRmRhdGFiYXNlc19nZXRfY2x1c3Rlcg

To show information about an existing database cluster, send a GET request to `/v2/databases/$DATABASE_ID`.
The response will be a JSON object with a database key. This will be set to an object containing the standard database cluster attributes.
The embedded connection and private_connection objects will contain the information needed to access the database cluster.
The embedded maintenance_window object will contain information about any scheduled maintenance for the database cluster.

```go
DatabasesGetCluster(
    ctx context.Context,
    databaseClusterUuid uuid.UUID) (
    models.ApiResponse[models.V2DatabasesResponse1],
    error)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `databaseClusterUuid` | `uuid.UUID` | Template, Required | A unique identifier for a database cluster. |


# Response Type

**200**: A JSON object with a key of `database`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.V2DatabasesResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v2-databases-response-1.md).


# Example Usage

```go
ctx := context.Background()

databaseClusterUuid := uuid.MustParse("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30")

apiResponse, err := databasesApi.DatabasesGetCluster(ctx, databaseClusterUuid)
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
  "database": {
    "connection": {
      "database": "",
      "host": "backend-do-user-19081923-0.db.ondigitalocean.com",
      "password": "wv78n3zpz42xezdk",
      "port": 25060,
      "ssl": true,
      "uri": "postgres://doadmin:wv78n3zpz42xezdk@backend-do-user-19081923-0.db.ondigitalocean.com:25060/defaultdb?sslmode=require",
      "user": "doadmin"
    },
    "created_at": "2019-01-11T18:37:36Z",
    "db_names": [
      "defaultdb"
    ],
    "engine": "pg",
    "id": "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    "maintenance_window": {
      "day": "saturday",
      "description": [
        "Update TimescaleDB to version 1.2.1",
        "Upgrade to PostgreSQL 11.2 and 10.7 bugfix releases"
      ],
      "hour": "08:45:12",
      "pending": true
    },
    "name": "backend",
    "num_nodes": 2,
    "private_connection": {
      "database": "",
      "host": "private-backend-do-user-19081923-0.db.ondigitalocean.com",
      "password": "wv78n3zpz42xezdk",
      "port": 25060,
      "ssl": true,
      "uri": "postgres://doadmin:wv78n3zpz42xezdk@private-backend-do-user-19081923-0.db.ondigitalocean.com:25060/defaultdb?sslmode=require",
      "user": "doadmin"
    },
    "private_network_uuid": "d455e75d-4858-4eec-8c95-da2f0a5f93a7",
    "region": "nyc3",
    "size": "db-s-2vcpu-4gb",
    "status": "creating",
    "tags": [
      "production"
    ],
    "users": [
      {
        "name": "doadmin",
        "password": "wv78n3zpz42xezdk",
        "role": "primary"
      }
    ],
    "version": "14",
    "version_end_of_availability": "2023-05-09T00:00:00Z",
    "version_end_of_life": "2023-11-09T00:00:00Z"
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



