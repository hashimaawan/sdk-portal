# Create Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZUltYWdlUmVxdWVzdA

*This model accepts additional fields of type array.*


# Class Name

`CreateImageRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `?string` | Optional | Description of the Image, will be auto-generated if not set | getDescription(): ?string | setDescription(?string description): void |
| `labels` | [`?Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) | getLabels(): ?Labels | setLabels(?Labels labels): void |
| `type` | [`?string(Type63)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-63.md) | Optional | Type of Image to create (default: `snapshot`) | getType(): ?string | setType(?string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\CreateImageRequestBuilder;
use HetznerCloudApiLib\Models\Builders\LabelsBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Type63;

$createImageRequest = CreateImageRequestBuilder::init()
    ->description('my image')
    ->labels(
        LabelsBuilder::init()
            ->labelkey('labelkey4')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->type(Type63::SNAPSHOT)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



