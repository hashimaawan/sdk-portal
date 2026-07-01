# Get a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZHZXQlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Returns a specific Floating IP object.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAFloatingIP(int $id): FloatingIpsResponse2
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |


# Response Type

**200**: The `floating_ip` key in the reply contains a Floating IP object with this structure

[`FloatingIpsResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/floating-ips-response-2.md)


# Example Usage

```php
$id = 112;

$floatingIPsController = $client->getFloatingIPsController();

try {
    $result = $floatingIPsController->getAFloatingIP($id);
    echo 'FloatingIpsResponse2:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



