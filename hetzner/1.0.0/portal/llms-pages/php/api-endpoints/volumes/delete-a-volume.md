# Delete a Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlZvbHVtZXMlMkZEZWxldGUlMjUyMGElMjUyMFZvbHVtZQ

Deletes a volume. All Volume data is irreversibly destroyed. The Volume must not be attached to a Server and it must not have delete protection enabled.

:information_source: **Note** This endpoint does not require authentication.

```php
function deleteAVolume(string $id): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | ID of the Volume |


# Response Type

**204**: Volume deleted

`void`


# Example Usage

```php
$id = 'id0';

$volumesController = $client->getVolumesController();

try {
    $volumesController->deleteAVolume($id);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



