# Get Session Status Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFNlc3Npb25TdGF0dXNSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`GetSessionStatusRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): string | setSessionId(string sessionId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetSessionStatusRequestBuilder;
use AmazonAthenaLib\ApiHelper;

$getSessionStatusRequest = GetSessionStatusRequestBuilder::init(
    'SessionId6'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



