# Delete a Primary IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRkRlbGV0ZSUyNTIwYSUyNTIwUHJpbWFyeSUyNTIwSVA

Deletes a Primary IP.

The Primary IP may be assigned to a Server. In this case it is unassigned automatically. The Server must be powered off (status `off`) in order for this operation to succeed.

:information_source: **Note** This endpoint does not require authentication.

```php
function deleteAPrimaryIP(int $id): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**204**: Primary IP deleted

`void`


# Example Usage

```php
$id = 112;

$primaryIPsController = $client->getPrimaryIPsController();

try {
    $primaryIPsController->deleteAPrimaryIP($id);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



