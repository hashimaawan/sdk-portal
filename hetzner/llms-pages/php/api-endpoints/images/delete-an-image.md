# Delete an Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0ZSUyRkltYWdlcyUyRkRlbGV0ZSUyNTIwYW4lMjUyMEltYWdl

Deletes an Image. Only Images of type `snapshot` and `backup` can be deleted.

:information_source: **Note** This endpoint does not require authentication.

```php
function deleteAnImage(int $id): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Image |


# Response Type

**204**: Image deleted

`void`


# Example Usage

```php
$id = 112;

$imagesController = $client->getImagesController();

try {
    $imagesController->deleteAnImage($id);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



