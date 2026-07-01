# Create a Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGQ3JlYXRlJTI1MjBhJTI1MjBQbGFjZW1lbnRHcm91cA

Creates a new PlacementGroup.

:information_source: **Note** This endpoint does not require authentication.

```php
function createAPlacementGroup(?CreatePlacementGroupRequest $body = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`?CreatePlacementGroupRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/create-placement-group-request.md) | Body, Optional | - |


# Response Type

**201**: The `PlacementGroup` key contains the PlacementGroup that was just created.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`CreatePlacementGroupResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/create-placement-group-response.md).


# Example Usage

```php
$body = CreatePlacementGroupRequestBuilder::init(
    'my Placement Group'
)->build();

$placementGroupsApi = $client->getPlacementGroupsApi();
$apiResponse = $placementGroupsApi->createAPlacementGroup($body);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'CreatePlacementGroupResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "placement_group": {
    "created": "2019-01-08T12:10:00+00:00",
    "id": 897,
    "labels": {
      "key": "value"
    },
    "name": "my Placement Group",
    "servers": [],
    "type": "spread"
  }
}
```



