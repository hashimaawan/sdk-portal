# Databases Add Connection Pool

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0ZSUyRkRhdGFiYXNlcyUyRmRhdGFiYXNlc19hZGRfY29ubmVjdGlvblBvb2w

For PostgreSQL database clusters, connection pools can be used to allow a
database to share its idle connections. The popular PostgreSQL connection
pooling utility PgBouncer is used to provide this service. [See here for more information](https://www.digitalocean.com/docs/databases/postgresql/how-to/manage-connection-pools/)
about how and why to use PgBouncer connection pooling including
details about the available transaction modes.

To add a new connection pool to a PostgreSQL database cluster, send a POST
request to `/v2/databases/$DATABASE_ID/pools` specifying a name for the pool,
the user to connect with, the database to connect to, as well as its desired
size and transaction mode.

```python
def databases_add_connection_pool(self,
                                 database_cluster_uuid,
                                 body)
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database_cluster_uuid` | `uuid\|str` | Template, Required | A unique identifier for a database cluster. |
| `body` | [`Pool`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/pool.md) | Body, Required | - |


# Response Type

**201**: A JSON object with a key of `pool`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`V2DatabasesPoolsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/v2-databases-pools-response-1.md).


# Example Usage

```python
database_cluster_uuid = '9cc10173-e9ea-4176-9dbc-a4cee4c4ff30'

body = Pool(
    db='defaultdb',
    mode='transaction',
    name='backend-pool',
    size=10,
    user='doadmin'
)

result = databases_api.databases_add_connection_pool(
    database_cluster_uuid,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response *(as JSON)*

```json
{
  "pool": {
    "connection": {
      "database": "backend-pool",
      "host": "backend-do-user-19081923-0.db.ondigitalocean.com",
      "password": "wv78n3zpz42xezdk",
      "port": 25061,
      "ssl": true,
      "uri": "postgres://doadmin:wv78n3zpz42xezdk@backend-do-user-19081923-0.db.ondigitalocean.com:25061/backend-pool?sslmode=require",
      "user": "doadmin"
    },
    "db": "defaultdb",
    "mode": "transaction",
    "name": "backend-pool",
    "size": 10,
    "user": "doadmin"
  }
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



