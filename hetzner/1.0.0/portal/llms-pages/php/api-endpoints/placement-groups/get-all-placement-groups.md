# Get All Placement Groups

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGR2V0JTI1MjBhbGwlMjUyMFBsYWNlbWVudEdyb3Vwcw

Returns all PlacementGroup objects.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllPlacementGroups(
    ?string $sort = null,
    ?string $name = null,
    ?string $labelSelector = null,
    ?string $type = null
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`?string(Sort)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `name` | `?string` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `?string` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `type` | [`?string(ParameterType1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/parameter-type-1.md) | Query, Optional | Can be used multiple times. The response will only contain PlacementGroups matching the type. |


# Response Type

**200**: The `placement_groups` key contains an array of PlacementGroup objects

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PlacementGroupsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/placement-groups-response.md).


# Example Usage

```php
$placementGroupsApi = $client->getPlacementGroupsApi();
$apiResponse = $placementGroupsApi->getAllPlacementGroups();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PlacementGroupsResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "placement_groups": [
    {
      "created": "2019-01-08T12:10:00+00:00",
      "id": 897,
      "labels": {
        "key": "value"
      },
      "name": "my Placement Group",
      "servers": [
        4711,
        4712
      ],
      "type": "spread"
    }
  ]
}
```



