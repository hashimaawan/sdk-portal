# Rule 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlJ1bGUx

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Rule1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `clusterUuid` | `?string` | Optional | A unique ID for the database cluster to which the rule is applied.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` | getClusterUuid(): ?string | setClusterUuid(?string clusterUuid): void |
| `createdAt` | `?DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the firewall rule was created. | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `type` | [`string(Type7)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/type-7.md) | Required | The type of resource that the firewall rule allows to access the database cluster. | getType(): string | setType(string type): void |
| `uuid` | `?string` | Optional | A unique ID for the firewall rule itself.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` | getUuid(): ?string | setUuid(?string uuid): void |
| `value` | `string` | Required | The ID of the specific resource, the name of a tag applied to a group of resources, or the IP address that the firewall rule allows to access the database cluster. | getValue(): string | setValue(string value): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Rule1Builder;
use DigitalOceanApiLib\Models\Type7;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\ApiHelper;

$rule1 = Rule1Builder::init(
    Type7::DROPLET,
    'ff2a6c52-5a44-4b63-b99c-0e98e7a63d61'
)
    ->clusterUuid('9cc10173-e9ea-4176-9dbc-a4cee4c4ff30')
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2019-01-11T18:37:36Z'))
    ->uuid('79f26d28-ea8a-41f2-8ad8-8cfcdd020095')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



