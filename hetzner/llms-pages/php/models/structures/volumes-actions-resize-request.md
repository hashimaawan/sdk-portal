# Volumes Actions Resize Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMFJlc2l6ZSUyNTIwUmVxdWVzdA


# Class Name

`VolumesActionsResizeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `size` | `float` | Required | New Volume size in GB (must be greater than current size) | getSize(): float | setSize(float size): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\VolumesActionsResizeRequestBuilder;

$volumesActionsResizeRequest = VolumesActionsResizeRequestBuilder::init(
    50
)->build();
```



