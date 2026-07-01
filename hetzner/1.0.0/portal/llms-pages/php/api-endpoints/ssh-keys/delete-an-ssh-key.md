# Delete an SSH Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkRlbGV0ZSUyNTIwYW4lMjUyMFNTSCUyNTIwa2V5

Deletes an SSH key. It cannot be used anymore.

:information_source: **Note** This endpoint does not require authentication.

```php
function deleteAnSSHKey(string $id): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | ID of the SSH key |


# Response Type

**204**: SSH key deleted

`void`


# Example Usage

```php
$id = 'id0';

$sSHKeysController = $client->getSSHKeysController();

try {
    $sSHKeysController->deleteAnSSHKey($id);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



