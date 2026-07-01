# Images Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0


# Class Name

`ImagesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `delete` | `?bool` | Optional | If true, prevents the snapshot from being deleted | getDelete(): ?bool | setDelete(?bool delete): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ImagesActionsChangeProtectionRequestBuilder;

$imagesActionsChangeProtectionRequest = ImagesActionsChangeProtectionRequestBuilder::init()
    ->delete(true)
    ->build();
```



