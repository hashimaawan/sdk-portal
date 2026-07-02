# Databases Create Cluster

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0ZSUyRkRhdGFiYXNlcyUyRmRhdGFiYXNlc19jcmVhdGVfY2x1c3Rlcg

To create a database cluster, send a POST request to `/v2/databases`.
The response will be a JSON object with a key called `database`. The value of this will be an object that contains the standard attributes associated with a database cluster. The initial value of the database cluster's `status` attribute will be `creating`. When the cluster is ready to receive traffic, this will transition to `online`.
The embedded `connection` and `private_connection` objects will contain the information needed to access the database cluster.
DigitalOcean managed PostgreSQL and MySQL database clusters take automated daily backups. To create a new database cluster based on a backup of an existing cluster, send a POST request to `/v2/databases`. In addition to the standard database cluster attributes, the JSON body must include a key named `backup_restore` with the name of the original database cluster and the timestamp of the backup to be restored. Creating a database from a backup is the same as forking a database in the control panel.
Note: Backups are not supported for Redis clusters.

```ts
async databasesCreateCluster(
  body: V2DatabasesRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<V2DatabasesResponse1>>
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V2DatabasesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-databases-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**201**: A JSON object with a key of `database`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`V2DatabasesResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-databases-response-1.md).


# Example Usage

```ts
const body: V2DatabasesRequest = {
  engine: Engine1.Pg,
  name: 'backend',
  numNodes: 2,
  region: 'nyc3',
  size: 'db-s-2vcpu-4gb',
  tags: [
    'production'
  ],
  version: '14',
};

try {
  const response = await databasesApi.databasesCreateCluster(body);

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
| 401 | Unauthorized | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/exceptions/v2-1-clicks-401-error.md) |



