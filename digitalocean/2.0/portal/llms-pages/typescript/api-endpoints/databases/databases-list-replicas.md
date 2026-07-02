# Databases List Replicas

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkRhdGFiYXNlcyUyRmRhdGFiYXNlc19saXN0X3JlcGxpY2Fz

To list all of the read-only replicas associated with a database cluster, send a GET request to `/v2/databases/$DATABASE_ID/replicas`.

**Note**: Read-only replicas are not supported for Redis clusters.

The result will be a JSON object with a `replicas` key. This will be set to an array of database replica objects, each of which will contain the standard database replica attributes.

```ts
async databasesListReplicas(
  databaseClusterUuid: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2DatabasesReplicasResponse>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `databaseClusterUuid` | `string` | Template, Required | A unique identifier for a database cluster. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: A JSON object with a key of `replicas`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2DatabasesReplicasResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-databases-replicas-response.md).


# Example Usage

```ts
const databaseClusterUuid = '9cc10173-e9ea-4176-9dbc-a4cee4c4ff30';

try {
  const response = await databasesApi.databasesListReplicas(databaseClusterUuid);

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
    if (error instanceof V21Clicks401Error) {
      console.log(error.result);
    }
  }
}
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
| 401 | Unauthorized | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |



