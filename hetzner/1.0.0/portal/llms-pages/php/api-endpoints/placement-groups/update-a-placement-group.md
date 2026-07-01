# Update a Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGVXBkYXRlJTI1MjBhJTI1MjBQbGFjZW1lbnRHcm91cA

Updates the PlacementGroup properties.

Note that when updating labels, the PlacementGroup’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

Note: if the PlacementGroup object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```php
function updateAPlacementGroup(int $id, ?UpdatePlacementGroupRequest $body = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |
| `body` | [`?UpdatePlacementGroupRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/update-placement-group-request.md) | Body, Optional | - |


# Response Type

**200**: The `certificate` key contains the PlacementGroup that was just updated

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PlacementGroupResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/placement-group-response.md).


# Example Usage

```php
$id = 112;

$body = UpdatePlacementGroupRequestBuilder::init()
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('my Placement Group')
    ->build();

$placementGroupsApi = $client->getPlacementGroupsApi();
$apiResponse = $placementGroupsApi->updateAPlacementGroup(
    $id,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PlacementGroupResponse:';
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
    "servers": [
      4711,
      4712
    ],
    "type": "spread"
  }
}
```



