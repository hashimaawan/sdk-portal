# Databases List Clusters

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkRhdGFiYXNlcyUyRmRhdGFiYXNlc19saXN0X2NsdXN0ZXJz

To list all of the database clusters available on your account, send a GET request to `/v2/databases`. To limit the results to database clusters with a specific tag, include the `tag_name` query parameter set to the name of the tag. For example, `/v2/databases?tag_name=$TAG_NAME`.
The result will be a JSON object with a `databases` key. This will be set to an array of database objects, each of which will contain the standard database attributes.
The embedded `connection` and `private_connection` objects will contain the information needed to access the database cluster:
The embedded `maintenance_window` object will contain information about any scheduled maintenance for the database cluster.

```php
function databasesListClusters(?string $tagName = null): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tagName` | `?string` | Query, Optional | Limits the results to database clusters with a specific tag. |


# Response Type

**200**: A JSON object with a key of `databases`.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2DatabasesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-databases-response.md).


# Example Usage

```php
$tagName = 'production';

$databasesApi = $client->getDatabasesApi();
$apiResponse = $databasesApi->databasesListClusters($tagName);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2DatabasesResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "databases": [
    {
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
      "num_nodes": 1,
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
      "status": "online",
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
      "version": "10",
      "version_end_of_availability": "2023-05-09T00:00:00Z",
      "version_end_of_life": "2023-11-09T00:00:00Z"
    }
  ]
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | The resource was not found. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |



