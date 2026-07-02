# Resources 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlJlc291cmNlczE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Resources1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `assignedAt` | `?DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the project was created. | getAssignedAt(): ?\DateTime | setAssignedAt(?\DateTime assignedAt): void |
| `links` | [`?Links4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/links-4.md) | Optional | The links object contains the `self` object, which contains the resource relationship. | getLinks(): ?Links4 | setLinks(?Links4 links): void |
| `status` | [`?string(Status14)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status-14.md) | Optional | The status of assigning and fetching the resources. | getStatus(): ?string | setStatus(?string status): void |
| `urn` | `?string` | Optional | The uniform resource name (URN) for the resource in the format do:resource_type:resource_id.<br><br>**Constraints**: *Pattern*: `^do:(dbaas\|domain\|droplet\|floatingip\|loadbalancer\|space\|volume\|kubernetes\|vpc):.*` | getUrn(): ?string | setUrn(?string urn): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Resources1Builder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\Links4Builder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Status14;

$resources1 = Resources1Builder::init()
    ->assignedAt(DateTimeHelper::fromRfc3339DateTime('2018-09-28T19:26:37Z'))
    ->links(
        Links4Builder::init()
            ->self('self2')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->status(Status14::OK)
    ->urn('do:droplet:13457723')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



