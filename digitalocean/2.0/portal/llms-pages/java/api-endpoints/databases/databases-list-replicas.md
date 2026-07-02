# Databases List Replicas

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0ZSUyRkRhdGFiYXNlcyUyRmRhdGFiYXNlc19saXN0X3JlcGxpY2Fz

To list all of the read-only replicas associated with a database cluster, send a GET request to `/v2/databases/$DATABASE_ID/replicas`.

**Note**: Read-only replicas are not supported for Redis clusters.

The result will be a JSON object with a `replicas` key. This will be set to an array of database replica objects, each of which will contain the standard database replica attributes.

```java
CompletableFuture<ApiResponse<V2DatabasesReplicasResponse>> databasesListReplicasAsync(
    final UUID databaseClusterUuid)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `databaseClusterUuid` | `UUID` | Template, Required | A unique identifier for a database cluster. |


# Response Type

**200**: A JSON object with a key of `replicas`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`V2DatabasesReplicasResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/v2-databases-replicas-response.md).


# Example Usage

```java
UUID databaseClusterUuid = UUID.fromString("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30");

databasesApi.databasesListReplicasAsync(databaseClusterUuid).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    Throwable cause = exception.getCause();

    if (cause instanceof V21Clicks401ErrorException) {
        V21Clicks401ErrorException v21Clicks401ErrorException = (V21Clicks401ErrorException) cause;
        v21Clicks401ErrorException.printStackTrace();
    } else {
        // fallback for unexpected errors
        exception.printStackTrace();
    }

    return null;
});
```


# Example Response *(as JSON)*

```json
{
  "replicas": [
    {
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
  ]
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/exceptions/v2-1-clicks-401-error.md) |



