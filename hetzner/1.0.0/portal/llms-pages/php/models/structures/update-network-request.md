# Update Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlVwZGF0ZU5ldHdvcmtSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`UpdateNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labels` | [`?Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) | getLabels(): ?Labels2 | setLabels(?Labels2 labels): void |
| `name` | `?string` | Optional | New network name | getName(): ?string | setName(?string name): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\UpdateNetworkRequestBuilder;
use HetznerCloudApiLib\Models\Builders\Labels2Builder;
use HetznerCloudApiLib\ApiHelper;

$updateNetworkRequest = UpdateNetworkRequestBuilder::init()
    ->labels(
        Labels2Builder::init()
            ->labelkey('labelkey4')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->name('new-name')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



