# V2 Projects Default Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2ProjectsDefaultResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `project` | [`?Project`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/project.md) | Optional | - | getProject(): ?Project | setProject(?Project project): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2ProjectsDefaultResponseBuilder;
use DigitalOceanApiLib\Models\Builders\ProjectBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Environment;
use DigitalOceanApiLib\ApiHelper;

$v2ProjectsDefaultResponse = V2ProjectsDefaultResponseBuilder::init()
    ->project(
        ProjectBuilder::init()
            ->createdAt(DateTimeHelper::fromRfc3339DateTime('2017-10-19T21:44:20Z'))
            ->description('Default project')
            ->environment(Environment::DEVELOPMENT)
            ->id('addb4547-6bab-419a-8542-76263a033cf6')
            ->name('Default')
            ->ownerId(258992)
            ->ownerUuid('99525febec065ca37b2ffe4f852fd2b2581895e7')
            ->purpose('Just trying out DigitalOcean')
            ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2019-11-05T18:50:03Z'))
            ->isDefault(true)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



