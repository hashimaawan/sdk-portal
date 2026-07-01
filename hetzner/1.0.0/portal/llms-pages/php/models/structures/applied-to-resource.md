# Applied to Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkFwcGxpZWRUb1Jlc291cmNl

*This model accepts additional fields of type array.*


# Class Name

`AppliedToResource`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `server` | [`?Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server.md) | Optional | - | getServer(): ?Server | setServer(?Server server): void |
| `type` | [`?string(Type5)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-5.md) | Optional | Type of resource referenced | getType(): ?string | setType(?string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\AppliedToResourceBuilder;
use HetznerCloudApiLib\Models\Builders\ServerBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Type5;

$appliedToResource = AppliedToResourceBuilder::init()
    ->server(
        ServerBuilder::init(
            14
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->type(Type5::SERVER)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



