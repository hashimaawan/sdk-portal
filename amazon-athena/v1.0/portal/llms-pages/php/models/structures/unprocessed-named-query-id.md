# Unprocessed Named Query Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkTmFtZWRRdWVyeUlk

Information about a named query ID that could not be processed.

*This model accepts additional fields of type array.*


# Class Name

`UnprocessedNamedQueryId`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `namedQueryId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getNamedQueryId(): ?string | setNamedQueryId(?string namedQueryId): void |
| `errorCode` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getErrorCode(): ?string | setErrorCode(?string errorCode): void |
| `errorMessage` | `?string` | Optional | - | getErrorMessage(): ?string | setErrorMessage(?string errorMessage): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\UnprocessedNamedQueryIdBuilder;
use AmazonAthenaLib\ApiHelper;

$unprocessedNamedQueryId = UnprocessedNamedQueryIdBuilder::init()
    ->namedQueryId('NamedQueryId0')
    ->errorCode('ErrorCode8')
    ->errorMessage('ErrorMessage8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



