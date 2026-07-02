# Start Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`StartSessionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): string | setWorkGroup(string workGroup): void |
| `engineConfiguration` | [`EngineConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/engine-configuration-1.md) | Required | - | getEngineConfiguration(): EngineConfiguration1 | setEngineConfiguration(EngineConfiguration1 engineConfiguration): void |
| `notebookVersion` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getNotebookVersion(): ?string | setNotebookVersion(?string notebookVersion): void |
| `sessionIdleTimeoutInMinutes` | `?int` | Optional | **Constraints**: `>= 1`, `<= 480` | getSessionIdleTimeoutInMinutes(): ?int | setSessionIdleTimeoutInMinutes(?int sessionIdleTimeoutInMinutes): void |
| `clientRequestToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` | getClientRequestToken(): ?string | setClientRequestToken(?string clientRequestToken): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\StartSessionRequestBuilder;
use AmazonAthenaLib\Models\Builders\EngineConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\AdditionalConfigsBuilder;
use AmazonAthenaLib\ApiHelper;

$startSessionRequest = StartSessionRequestBuilder::init(
    'WorkGroup2',
    EngineConfiguration1Builder::init(
        94
    )
        ->coordinatorDpuSize(1)
        ->defaultExecutorDpuSize(1)
        ->additionalConfigs(
            AdditionalConfigsBuilder::init()
                ->additionalProperty('exampleAdditionalProperty', 'AdditionalConfigs_additionalProperties5')
                ->build()
        )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->description('Description4')
    ->notebookVersion('NotebookVersion4')
    ->sessionIdleTimeoutInMinutes(172)
    ->clientRequestToken('ClientRequestToken4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



