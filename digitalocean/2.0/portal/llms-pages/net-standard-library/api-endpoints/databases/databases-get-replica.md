# Databases Get Replica

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkRhdGFiYXNlcyUyRmRhdGFiYXNlc19nZXRfcmVwbGljYQ

To show information about an existing database replica, send a GET request to `/v2/databases/$DATABASE_ID/replicas/$REPLICA_NAME`.

**Note**: Read-only replicas are not supported for Redis clusters.

The response will be a JSON object with a `replica key`. This will be set to an object containing the standard database replica attributes.

```csharp
DatabasesGetReplicaAsync(
    Guid databaseClusterUuid,
    string replicaName)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `databaseClusterUuid` | `Guid` | Template, Required | A unique identifier for a database cluster. |
| `replicaName` | `string` | Template, Required | The name of the database replica. |


# Response Type

**200**: A JSON object with a key of `replica`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.V2DatabasesReplicasResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/v2-databases-replicas-response-1.md).


# Example Usage

```csharp
Guid databaseClusterUuid = new Guid("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30");
string replicaName = "read-nyc3-01";
try
{
    ApiResponse<V2DatabasesReplicasResponse1> result = await databasesApi.DatabasesGetReplicaAsync(
        databaseClusterUuid,
        replicaName
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
  "replica": {
    "connection": {
      "database": "defaultdb",
      "host": "read-nyc3-01-do-user-19081923-0.db.ondigitalocean.com",
      "password": "wv78n3zpz42xezdk",
      "port": 25060,
      "ssl": true,
      "uri": "",
      "user": "doadmin"
    },
    "created_at": "2019-01-11T18:37:36Z",
    "name": "read-nyc3-01",
    "private_connection": {
      "database": "",
      "host": "private-read-nyc3-01-do-user-19081923-0.db.ondigitalocean.com",
      "password": "wv78n3zpz42xezdk",
      "port": 25060,
      "ssl": true,
      "uri": "postgres://doadmin:wv78n3zpz42xezdk@private-read-nyc3-01-do-user-19081923-0.db.ondigitalocean.com:25060/defaultdb?sslmode=require",
      "user": "doadmin"
    },
    "region": "nyc3",
    "status": "online"
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



