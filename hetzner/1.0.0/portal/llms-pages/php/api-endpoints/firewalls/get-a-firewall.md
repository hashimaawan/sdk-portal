# Get a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRkdldCUyNTIwYSUyNTIwRmlyZXdhbGw

Gets a specific Firewall object.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAFirewall(int $id): FirewallResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**200**: The `firewall` key contains a Firewall object

[`FirewallResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/firewall-response.md)


# Example Usage

```php
$id = 112;

$firewallsController = $client->getFirewallsController();

try {
    $result = $firewallsController->getAFirewall($id);
    echo 'FirewallResponse:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



