# Start Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`StartCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): string | setSessionId(string sessionId): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `calculationConfiguration` | [`?GetCalculationExecutionCodeResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/get-calculation-execution-code-response.md) | Optional | - | getCalculationConfiguration(): ?GetCalculationExecutionCodeResponse | setCalculationConfiguration(?GetCalculationExecutionCodeResponse calculationConfiguration): void |
| `codeBlock` | `?string` | Optional | **Constraints**: *Maximum Length*: `68000` | getCodeBlock(): ?string | setCodeBlock(?string codeBlock): void |
| `clientRequestToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` | getClientRequestToken(): ?string | setClientRequestToken(?string clientRequestToken): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\StartCalculationExecutionRequestBuilder;
use AmazonAthenaLib\Models\Builders\GetCalculationExecutionCodeResponseBuilder;
use AmazonAthenaLib\ApiHelper;

$startCalculationExecutionRequest = StartCalculationExecutionRequestBuilder::init(
    'SessionId4'
)
    ->description('Description2')
    ->calculationConfiguration(
        GetCalculationExecutionCodeResponseBuilder::init()
            ->codeBlock('CodeBlock4')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->codeBlock('CodeBlock6')
    ->clientRequestToken('ClientRequestToken8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



