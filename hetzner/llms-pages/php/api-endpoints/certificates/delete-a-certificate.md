# Delete a Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0ZSUyRkNlcnRpZmljYXRlcyUyRkRlbGV0ZSUyNTIwYSUyNTIwQ2VydGlmaWNhdGU

Deletes a Certificate.

:information_source: **Note** This endpoint does not require authentication.

```php
function deleteACertificate(int $id): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**204**: Certificate deleted

`void`


# Example Usage

```php
$id = 112;

$certificatesController = $client->getCertificatesController();

try {
    $certificatesController->deleteACertificate($id);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



