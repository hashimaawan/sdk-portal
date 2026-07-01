# Update Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlVwZGF0ZVZvbHVtZVJlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`UpdateVolumeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labels` | [`?Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) | getLabels(): ?Labels2 | setLabels(?Labels2 labels): void |
| `name` | `string` | Required | New Volume name | getName(): string | setName(string name): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\UpdateVolumeRequestBuilder;
use HetznerCloudApiLib\Models\Builders\Labels2Builder;
use HetznerCloudApiLib\ApiHelper;

$updateVolumeRequest = UpdateVolumeRequestBuilder::init(
    'database-storage'
)
    ->labels(
        Labels2Builder::init()
            ->labelkey('labelkey4')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



