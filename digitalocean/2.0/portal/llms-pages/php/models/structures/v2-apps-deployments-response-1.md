# V2 Apps Deployments Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBEZXBsb3ltZW50cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AppsDeploymentsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `deployment` | [`?AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/an-app-deployment.md) | Optional | - | getDeployment(): ?AnAppDeployment | setDeployment(?AnAppDeployment deployment): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AppsDeploymentsResponse1Builder;
use DigitalOceanApiLib\Models\Builders\AnAppDeploymentBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\FunctionsComponentsThatArePartOfThisDeploymentBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2AppsDeploymentsResponse1 = V2AppsDeploymentsResponse1Builder::init()
    ->deployment(
        AnAppDeploymentBuilder::init()
            ->cause('cause8')
            ->clonedFrom('cloned_from0')
            ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->functions(
                [
                    FunctionsComponentsThatArePartOfThisDeploymentBuilder::init()
                        ->name('name4')
                        ->namespace('namespace8')
                        ->sourceCommitHash('source_commit_hash4')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ]
            )
            ->id('id2')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



