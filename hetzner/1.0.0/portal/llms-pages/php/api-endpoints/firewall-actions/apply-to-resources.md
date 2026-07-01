# Apply to Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkZpcmV3YWxsJTI1MjBBY3Rpb25zJTJGQXBwbHklMjUyMHRvJTI1MjBSZXNvdXJjZXM

Applies one Firewall to multiple resources.

Currently servers (public network interface) and label selectors are supported.

#### Call specific error codes

| Code                          | Description                                                   |
|-------------------------------|---------------------------------------------------------------|
| `firewall_already_applied`    | Firewall was already applied on resource                      |
| `incompatible_network_type`   | The Network type is incompatible for the given resource       |
| `firewall_resource_not_found` | The resource the Firewall should be attached to was not found |

:information_source: **Note** This endpoint does not require authentication.

```php
function applyToResources(int $id, ?ApplyToResourcesRequest $body = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Firewall |
| `body` | [`?ApplyToResourcesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/apply-to-resources-request.md) | Body, Optional | - |


# Response Type

**201**: The `actions` key contains multiple `apply_firewall` Actions

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/actions-response.md).


# Example Usage

```php
$id = 112;

$body = ApplyToResourcesRequestBuilder::init(
    [
        FirewallApplyToResourcesBuilder::init()
            ->server(
                Server9Builder::init(
                    42
                )->build()
            )
            ->type(Type7::SERVER)
            ->build()
    ]
)->build();

$firewallActionsApi = $client->getFirewallActionsApi();
$apiResponse = $firewallActionsApi->applyToResources(
    $id,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ActionsResponse:';
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
      "command": "apply_firewall",
      "error": {
        "code": "action_failed",
        "message": "Action failed"
      },
      "finished": "2016-01-30T23:56:00+00:00",
      "id": 14,
      "progress": 100,
      "resources": [
        {
          "id": 42,
          "type": "server"
        },
        {
          "id": 38,
          "type": "firewall"
        }
      ],
      "started": "2016-01-30T23:55:00+00:00",
      "status": "success"
    }
  ]
}
```



