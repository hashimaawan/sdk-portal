# Start Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`StartSessionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sessionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): ?string | setSessionId(?string sessionId): void |
| `state` | [`?string(SessionState1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/session-state-1.md) | Optional | - | getState(): ?string | setState(?string state): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\StartSessionResponseBuilder;
use AmazonAthenaLib\Models\SessionState1;
use AmazonAthenaLib\ApiHelper;

$startSessionResponse = StartSessionResponseBuilder::init()
    ->sessionId('SessionId4')
    ->state(SessionState1::CREATING)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



