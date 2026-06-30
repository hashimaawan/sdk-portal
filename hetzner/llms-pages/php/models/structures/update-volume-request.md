# Update Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlVwZGF0ZVZvbHVtZVJlcXVlc3Q


# Class Name

`UpdateVolumeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labels` | [`?Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) | getLabels(): ?Labels2 | setLabels(?Labels2 labels): void |
| `name` | `string` | Required | New Volume name | getName(): string | setName(string name): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\UpdateVolumeRequestBuilder;
use HetznerCloudAPILib\Models\Builders\Labels2Builder;

$updateVolumeRequest = UpdateVolumeRequestBuilder::init(
    'database-storage'
)
    ->labels(
        Labels2Builder::init()
            ->labelkey('labelkey4')
            ->build()
    )
    ->build();
```



