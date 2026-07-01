# Volumes Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA


# Class Name

`VolumesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `delete` | `?bool` | Optional | If true, prevents the Volume from being deleted | getDelete(): ?bool | setDelete(?bool delete): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\VolumesActionsChangeProtectionRequestBuilder;

$volumesActionsChangeProtectionRequest = VolumesActionsChangeProtectionRequestBuilder::init()
    ->delete(true)
    ->build();
```



