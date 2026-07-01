# Delete a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZEZWxldGUlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Deletes a Floating IP. If it is currently assigned to a Server it will automatically get unassigned.

:information_source: **Note** This endpoint does not require authentication.

```php
function deleteAFloatingIP(int $id): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |


# Response Type

**204**: Floating IP deleted

`void`


# Example Usage

```php
$id = 112;

$floatingIPsController = $client->getFloatingIPsController();

try {
    $floatingIPsController->deleteAFloatingIP($id);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



