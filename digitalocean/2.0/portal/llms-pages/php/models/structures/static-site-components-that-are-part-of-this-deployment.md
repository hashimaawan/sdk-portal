# Static Site Components that Are Part of This Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXRpYyUyNTIwU2l0ZSUyNTIwY29tcG9uZW50cyUyNTIwdGhhdCUyNTIwYXJlJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhpcyUyNTIwZGVwbG95bWVudA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`StaticSiteComponentsThatArePartOfThisDeployment`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | - | getName(): ?string | setName(?string name): void |
| `sourceCommitHash` | `?string` | Optional | - | getSourceCommitHash(): ?string | setSourceCommitHash(?string sourceCommitHash): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\StaticSiteComponentsThatArePartOfThisDeploymentBuilder;
use DigitalOceanApiLib\ApiHelper;

$staticSiteComponentsThatArePartOfThisDeployment = StaticSiteComponentsThatArePartOfThisDeploymentBuilder::init()
    ->name('web')
    ->sourceCommitHash('54d4a727f457231062439895000d45437c7bb405')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



