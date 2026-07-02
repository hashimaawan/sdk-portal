# V2 Registry Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2RegistryRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | A globally unique name for the container registry. Must be lowercase and be composed only of numbers, letters and `-`, up to a limit of 63 characters.<br><br>**Constraints**: *Maximum Length*: `63`, *Pattern*: `^[a-z0-9-]{1,63}$` | getName(): string | setName(string name): void |
| `region` | [`?string(Region6)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/region-6.md) | Optional | Slug of the region where registry data is stored. When not provided, a region will be selected. | getRegion(): ?string | setRegion(?string region): void |
| `subscriptionTierSlug` | [`string(SubscriptionTierSlug)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/subscription-tier-slug.md) | Required | The slug of the subscription tier to sign up for. Valid values can be retrieved using the options endpoint. | getSubscriptionTierSlug(): string | setSubscriptionTierSlug(string subscriptionTierSlug): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2RegistryRequestBuilder;
use DigitalOceanApiLib\Models\SubscriptionTierSlug;
use DigitalOceanApiLib\Models\Region6;
use DigitalOceanApiLib\ApiHelper;

$v2RegistryRequest = V2RegistryRequestBuilder::init(
    'example',
    SubscriptionTierSlug::BASIC
)
    ->region(Region6::FRA1)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



