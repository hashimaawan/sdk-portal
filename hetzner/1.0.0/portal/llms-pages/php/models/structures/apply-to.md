# Apply To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkFwcGx5VG8

*This model accepts additional fields of type array.*


# Class Name

`ApplyTo`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labelSelector` | [`?LabelSelector1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/label-selector-1.md) | Optional | Configuration for type LabelSelector, required if type is `label_selector` | getLabelSelector(): ?LabelSelector1 | setLabelSelector(?LabelSelector1 labelSelector): void |
| `server` | [`?Server2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-2.md) | Optional | Configuration for type Server, required if type is `server` | getServer(): ?Server2 | setServer(?Server2 server): void |
| `type` | [`string(Type7)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-7.md) | Required | Type of the resource | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ApplyToBuilder;
use HetznerCloudApiLib\Models\Type7;
use HetznerCloudApiLib\Models\Builders\LabelSelector1Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\Server2Builder;

$applyTo = ApplyToBuilder::init(
    Type7::SERVER
)
    ->labelSelector(
        LabelSelector1Builder::init(
            'selector8'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->server(
        Server2Builder::init(
            14
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



