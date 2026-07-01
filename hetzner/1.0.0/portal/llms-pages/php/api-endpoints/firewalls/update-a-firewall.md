# Update a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRlVwZGF0ZSUyNTIwYSUyNTIwRmlyZXdhbGw

Updates the Firewall.

Note that when updating labels, the Firewall's current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

Note: if the Firewall object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```php
function updateAFirewall(int $id, ?UpdateFirewallRequest $body = null): FirewallResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |
| `body` | [`?UpdateFirewallRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/update-firewall-request.md) | Body, Optional | - |


# Response Type

**200**: The `firewall` key contains the Firewall that was just updated

[`FirewallResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/firewall-response.md)


# Example Usage

```php
$id = 112;

$body = UpdateFirewallRequestBuilder::init()
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('new-name')
    ->build();

$firewallsController = $client->getFirewallsController();

try {
    $result = $firewallsController->updateAFirewall(
        $id,
        $body
    );
    echo 'FirewallResponse:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



