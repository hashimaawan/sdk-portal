# Applied To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkFwcGxpZWRUbw

*This model accepts additional fields of type array.*


# Class Name

`AppliedTo`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `appliedToResources` | [`?(AppliedToResource[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/applied-to-resource.md) | Optional | - | getAppliedToResources(): ?array | setAppliedToResources(?array appliedToResources): void |
| `labelSelector` | [`?LabelSelector`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/label-selector.md) | Optional | - | getLabelSelector(): ?LabelSelector | setLabelSelector(?LabelSelector labelSelector): void |
| `server` | [`?Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server.md) | Optional | - | getServer(): ?Server | setServer(?Server server): void |
| `type` | [`string(Type6)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-6.md) | Required | Type of resource referenced | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\AppliedToBuilder;
use HetznerCloudApiLib\Models\Type6;
use HetznerCloudApiLib\Models\Builders\AppliedToResourceBuilder;
use HetznerCloudApiLib\Models\Builders\ServerBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Type5;
use HetznerCloudApiLib\Models\Builders\LabelSelectorBuilder;

$appliedTo = AppliedToBuilder::init(
    Type6::SERVER
)
    ->appliedToResources(
        [
            AppliedToResourceBuilder::init()
                ->server(
                    ServerBuilder::init(
                        14
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->type(Type5::SERVER)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            AppliedToResourceBuilder::init()
                ->server(
                    ServerBuilder::init(
                        14
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->type(Type5::SERVER)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->labelSelector(
        LabelSelectorBuilder::init(
            'selector8'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->server(
        ServerBuilder::init(
            14
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



