# Named Query 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRk5hbWVkUXVlcnkx

*This model accepts additional fields of type array.*


# Class Name

`NamedQuery1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getName(): string | setName(string name): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `database` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | getDatabase(): string | setDatabase(string database): void |
| `queryString` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` | getQueryString(): string | setQueryString(string queryString): void |
| `namedQueryId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getNamedQueryId(): ?string | setNamedQueryId(?string namedQueryId): void |
| `workGroup` | `?string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): ?string | setWorkGroup(?string workGroup): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\NamedQuery1Builder;
use AmazonAthenaLib\ApiHelper;

$namedQuery1 = NamedQuery1Builder::init(
    'Name0',
    'Database8',
    'QueryString2'
)
    ->description('Description6')
    ->namedQueryId('NamedQueryId2')
    ->workGroup('WorkGroup2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



