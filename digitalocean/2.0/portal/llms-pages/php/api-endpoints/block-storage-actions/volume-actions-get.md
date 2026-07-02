# Volume Actions Get

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkJsb2NrJTI1MjBTdG9yYWdlJTI1MjBBY3Rpb25zJTJGdm9sdW1lQWN0aW9uc19nZXQ

To retrieve the status of a volume action, send a GET request to `/v2/volumes/$VOLUME_ID/actions/$ACTION_ID`.

```php
function volumeActionsGet(string $volumeId, int $actionId, ?int $perPage = 20, ?int $page = 1): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `volumeId` | `string` | Template, Required | The ID of the block storage volume. |
| `actionId` | `int` | Template, Required | A unique numeric ID that can be used to identify and reference an action.<br><br>**Constraints**: `>= 1` |
| `perPage` | `?int` | Query, Optional | Number of items returned per page<br><br>**Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 200` |
| `page` | `?int` | Query, Optional | Which 'page' of paginated results to return.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |


# Response Type

**200**: The response will be an object with a key called `action`. The value of this will be an object that contains the standard volume action attributes

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2VolumesActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-volumes-actions-response.md).


# Example Usage

```php
$volumeId = '7724db7c-e098-11e5-b522-000f53304e51';

$actionId = 36804636;

$perPage = 2;

$page = 1;

$blockStorageActionsApi = $client->getBlockStorageActionsApi();
$apiResponse = $blockStorageActionsApi->volumeActionsGet(
    $volumeId,
    $actionId,
    $perPage,
    $page
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2VolumesActionsResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "completed_at": null,
    "id": 68212773,
    "region": {
      "available": true,
      "features": [
        "private_networking",
        "backups",
        "ipv6",
        "metadata"
      ],
      "name": "New York 1",
      "sizes": [
        "s-1vcpu-1gb",
        "s-1vcpu-2gb",
        "s-1vcpu-3gb",
        "s-2vcpu-2gb",
        "s-3vcpu-1gb",
        "s-2vcpu-4gb",
        "s-4vcpu-8gb",
        "s-6vcpu-16gb",
        "s-8vcpu-32gb",
        "s-12vcpu-48gb",
        "s-16vcpu-64gb",
        "s-20vcpu-96gb",
        "s-24vcpu-128gb",
        "s-32vcpu-192gb"
      ],
      "slug": "nyc1"
    },
    "region_slug": "nyc1",
    "resource_id": null,
    "resource_type": "backend",
    "started_at": "2015-10-15T17:46:15Z",
    "status": "in-progress",
    "type": "detach_volume"
  }
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



