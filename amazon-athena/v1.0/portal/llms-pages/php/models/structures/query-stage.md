# Query Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2U

Stage statistics such as input and output rows and bytes, execution time and stage state. This information also includes substages and the query stage plan.

*This model accepts additional fields of type array.*


# Class Name

`QueryStage`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `stageId` | `?int` | Optional | - | getStageId(): ?int | setStageId(?int stageId): void |
| `state` | `?string` | Optional | - | getState(): ?string | setState(?string state): void |
| `outputBytes` | `?int` | Optional | - | getOutputBytes(): ?int | setOutputBytes(?int outputBytes): void |
| `outputRows` | `?int` | Optional | - | getOutputRows(): ?int | setOutputRows(?int outputRows): void |
| `inputBytes` | `?int` | Optional | - | getInputBytes(): ?int | setInputBytes(?int inputBytes): void |
| `inputRows` | `?int` | Optional | - | getInputRows(): ?int | setInputRows(?int inputRows): void |
| `executionTime` | `?int` | Optional | - | getExecutionTime(): ?int | setExecutionTime(?int executionTime): void |
| `queryStagePlan` | [`?QueryStagePlan`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/query-stage-plan.md) | Optional | - | getQueryStagePlan(): ?QueryStagePlan | setQueryStagePlan(?QueryStagePlan queryStagePlan): void |
| `subStages` | [`?(QueryStage[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/query-stage.md) | Optional | - | getSubStages(): ?array | setSubStages(?array subStages): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\QueryStageBuilder;
use AmazonAthenaLib\ApiHelper;

$queryStage = QueryStageBuilder::init()
    ->stageId(118)
    ->state('State0')
    ->outputBytes(120)
    ->outputRows(146)
    ->inputBytes(178)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



