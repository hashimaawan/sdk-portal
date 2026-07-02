# Named Query

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRk5hbWVkUXVlcnk

A query, where <code>QueryString</code> contains the SQL statements that make up the query.

*This model accepts additional fields of type array.*


# Class Name

`NamedQuery`


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
use AmazonAthenaLib\Models\Builders\NamedQueryBuilder;
use AmazonAthenaLib\ApiHelper;

$namedQuery = NamedQueryBuilder::init(
    'Name8',
    'Database0',
    'QueryString4'
)
    ->description('Description4')
    ->namedQueryId('NamedQueryId0')
    ->workGroup('WorkGroup4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



