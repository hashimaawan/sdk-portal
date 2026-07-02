# Project

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlByb2plY3Q

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Project`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `createdAt` | `?DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the project was created. | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `description` | `?string` | Optional | The description of the project. The maximum length is 255 characters.<br><br>**Constraints**: *Maximum Length*: `255` | getDescription(): ?string | setDescription(?string description): void |
| `environment` | [`?string(Environment)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/environment.md) | Optional | The environment of the project's resources. | getEnvironment(): ?string | setEnvironment(?string environment): void |
| `id` | `?string` | Optional, Read-only | The unique universal identifier of this project. | getId(): ?string | setId(?string id): void |
| `name` | `?string` | Optional | The human-readable name for the project. The maximum length is 175 characters and the name must be unique.<br><br>**Constraints**: *Maximum Length*: `175` | getName(): ?string | setName(?string name): void |
| `ownerId` | `?int` | Optional, Read-only | The integer id of the project owner. | getOwnerId(): ?int | setOwnerId(?int ownerId): void |
| `ownerUuid` | `?string` | Optional, Read-only | The unique universal identifier of the project owner. | getOwnerUuid(): ?string | setOwnerUuid(?string ownerUuid): void |
| `purpose` | `?string` | Optional | The purpose of the project. The maximum length is 255 characters. It can<br>have one of the following values:<br><br>- Just trying out DigitalOcean<br>- Class project / Educational purposes<br>- Website or blog<br>- Web Application<br>- Service or API<br>- Mobile Application<br>- Machine learning / AI / Data processing<br>- IoT<br>- Operational / Developer tooling<br><br>If another value for purpose is specified, for example, "your custom purpose",<br>your purpose will be stored as `Other: your custom purpose`.<br><br>**Constraints**: *Maximum Length*: `255` | getPurpose(): ?string | setPurpose(?string purpose): void |
| `updatedAt` | `?DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the project was updated. | getUpdatedAt(): ?\DateTime | setUpdatedAt(?\DateTime updatedAt): void |
| `isDefault` | `?bool` | Optional | If true, all resources will be added to this project if no project is specified. | getIsDefault(): ?bool | setIsDefault(?bool isDefault): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ProjectBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Environment;
use DigitalOceanApiLib\ApiHelper;

$project = ProjectBuilder::init()
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2018-09-27T20:10:35Z'))
    ->description('My website API')
    ->environment(Environment::PRODUCTION)
    ->id('4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679')
    ->name('my-web-api')
    ->ownerId(258992)
    ->ownerUuid('99525febec065ca37b2ffe4f852fd2b2581895e7')
    ->purpose('Service or API')
    ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2018-09-27T20:10:35Z'))
    ->isDefault(false)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



