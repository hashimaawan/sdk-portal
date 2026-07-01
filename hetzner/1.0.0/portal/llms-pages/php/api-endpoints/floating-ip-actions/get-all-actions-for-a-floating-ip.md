# Get All Actions for a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUCUyNTIwQWN0aW9ucyUyRkdldCUyNTIwYWxsJTI1MjBBY3Rpb25zJTI1MjBmb3IlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Returns all Action objects for a Floating IP. You can sort the results by using the `sort` URI parameter, and filter them with the `status` parameter.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllActionsForAFloatingIp(int $id, ?string $sort = null, ?string $status = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |
| `sort` | [`?string(ParameterSort)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/parameter-sort.md) | Query, Optional | Can be used multiple times. |
| `status` | [`?string(ParameterStatus)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/parameter-status.md) | Query, Optional | Can be used multiple times, the response will contain only Actions with specified statuses |


# Response Type

**200**: The `actions` key contains a list of Actions

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`FloatingIpsActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/floating-ips-actions-response.md).


# Example Usage

```php
$id = 112;

$floatingIpActionsApi = $client->getFloatingIpActionsApi();
$apiResponse = $floatingIpActionsApi->getAllActionsForAFloatingIp($id);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'FloatingIpsActionsResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Example Response *(as JSON)*

```json
{
  "actions": [
    {
      "command": "assign_floating_ip",
      "error": {
        "code": "action_failed",
        "message": "Action failed"
      },
      "finished": "2016-01-30T23:56:00+00:00",
      "id": 13,
      "progress": 100,
      "resources": [
        {
          "id": 4711,
          "type": "server"
        },
        {
          "id": 4712,
          "type": "floating_ip"
        }
      ],
      "started": "2016-01-30T23:55:00+00:00",
      "status": "success"
    }
  ]
}
```



