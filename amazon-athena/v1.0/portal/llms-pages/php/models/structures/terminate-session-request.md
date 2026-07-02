# Terminate Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlRlcm1pbmF0ZVNlc3Npb25SZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`TerminateSessionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): string | setSessionId(string sessionId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\TerminateSessionRequestBuilder;
use AmazonAthenaLib\ApiHelper;

$terminateSessionRequest = TerminateSessionRequestBuilder::init(
    'SessionId0'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



