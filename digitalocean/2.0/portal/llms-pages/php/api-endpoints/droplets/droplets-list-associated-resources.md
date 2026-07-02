# Droplets List Associated Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkRyb3BsZXRzJTJGZHJvcGxldHNfbGlzdF9hc3NvY2lhdGVkUmVzb3VyY2Vz

To list the associated billable resources that can be destroyed along with a
Droplet, send a GET request to the
`/v2/droplets/$DROPLET_ID/destroy_with_associated_resources` endpoint.

The response will be a JSON object containing `snapshots`, `volumes`, and
`volume_snapshots` keys. Each will be set to an array of objects containing
information about the associated resources.

```php
function dropletsListAssociatedResources(int $dropletId): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dropletId` | `int` | Template, Required | A unique identifier for a Droplet instance.<br><br>**Constraints**: `>= 1` |


# Response Type

**200**: A JSON object containing `snapshots`, `volumes`, and `volume_snapshots` keys.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2DropletsDestroyWithAssociatedResourcesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-droplets-destroy-with-associated-resources-response.md).


# Example Usage

```php
$dropletId = 3164444;

$dropletsApi = $client->getDropletsApi();
$apiResponse = $dropletsApi->dropletsListAssociatedResources($dropletId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2DropletsDestroyWithAssociatedResourcesResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "floating_ips": [
    {
      "cost": "4.00",
      "id": "6186916",
      "name": "45.55.96.47"
    }
  ],
  "reserved_ips": [
    {
      "cost": "4.00",
      "id": "6186916",
      "name": "45.55.96.47"
    }
  ],
  "snapshots": [
    {
      "cost": "0.05",
      "id": "61486916",
      "name": "ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330"
    }
  ],
  "volume_snapshots": [
    {
      "cost": "0.04",
      "id": "edb0478d-7436-11ea-86e6-0a58ac144b91",
      "name": "volume-nyc1-01-1585758983629"
    }
  ],
  "volumes": [
    {
      "cost": "10.00",
      "id": "ba49449a-7435-11ea-b89e-0a58ac14480f",
      "name": "volume-nyc1-01"
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



