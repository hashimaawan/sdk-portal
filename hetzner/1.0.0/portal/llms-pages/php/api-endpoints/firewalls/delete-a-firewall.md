# Delete a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRkRlbGV0ZSUyNTIwYSUyNTIwRmlyZXdhbGw

Deletes a Firewall.

#### Call specific error codes

| Code                 | Description                               |
|--------------------- |-------------------------------------------|
| `resource_in_use`    | Firewall must not be in use to be deleted |

:information_source: **Note** This endpoint does not require authentication.

```php
function deleteAFirewall(int $id): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**204**: Firewall deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$id = 112;

$firewallsApi = $client->getFirewallsApi();
$apiResponse = $firewallsApi->deleteAFirewall($id);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'void:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



