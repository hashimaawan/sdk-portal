# Get Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFNlc3Npb25SZXNwb25zZQ

*This model accepts additional fields of type array.*


# Class Name

`GetSessionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sessionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): ?string | setSessionId(?string sessionId): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `workGroup` | `?string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): ?string | setWorkGroup(?string workGroup): void |
| `engineVersion` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getEngineVersion(): ?string | setEngineVersion(?string engineVersion): void |
| `engineConfiguration` | [`?EngineConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/engine-configuration-1.md) | Optional | - | getEngineConfiguration(): ?EngineConfiguration1 | setEngineConfiguration(?EngineConfiguration1 engineConfiguration): void |
| `notebookVersion` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getNotebookVersion(): ?string | setNotebookVersion(?string notebookVersion): void |
| `sessionConfiguration` | [`?SessionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/session-configuration-2.md) | Optional | - | getSessionConfiguration(): ?SessionConfiguration2 | setSessionConfiguration(?SessionConfiguration2 sessionConfiguration): void |
| `status` | [`?Status3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/status-3.md) | Optional | - | getStatus(): ?Status3 | setStatus(?Status3 status): void |
| `statistics` | [`?Statistics3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/statistics-3.md) | Optional | - | getStatistics(): ?Statistics3 | setStatistics(?Statistics3 statistics): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetSessionResponseBuilder;
use AmazonAthenaLib\Models\Builders\EngineConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\AdditionalConfigsBuilder;
use AmazonAthenaLib\ApiHelper;

$getSessionResponse = GetSessionResponseBuilder::init()
    ->sessionId('SessionId6')
    ->description('Description4')
    ->workGroup('WorkGroup4')
    ->engineVersion('EngineVersion8')
    ->engineConfiguration(
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
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



