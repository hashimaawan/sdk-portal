# List Work Groups Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RXb3JrR3JvdXBzT3V0cHV0

*This model accepts additional fields of type array.*


# Class Name

`ListWorkGroupsOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `workGroups` | [`?(WorkGroupSummary[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/work-group-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `50` | getWorkGroups(): ?array | setWorkGroups(?array workGroups): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListWorkGroupsOutputBuilder;
use AmazonAthenaLib\Models\Builders\WorkGroupSummaryBuilder;
use AmazonAthenaLib\Models\WorkGroupState1;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\Builders\EngineVersion1Builder;
use AmazonAthenaLib\ApiHelper;

$listWorkGroupsOutput = ListWorkGroupsOutputBuilder::init()
    ->workGroups(
        [
            WorkGroupSummaryBuilder::init()
                ->name('Name4')
                ->state(WorkGroupState1::ENABLED)
                ->description('Description0')
                ->creationTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->engineVersion(
                    EngineVersion1Builder::init()
                        ->selectedEngineVersion('SelectedEngineVersion4')
                        ->effectiveEngineVersion('EffectiveEngineVersion6')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            WorkGroupSummaryBuilder::init()
                ->name('Name4')
                ->state(WorkGroupState1::ENABLED)
                ->description('Description0')
                ->creationTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->engineVersion(
                    EngineVersion1Builder::init()
                        ->selectedEngineVersion('SelectedEngineVersion4')
                        ->effectiveEngineVersion('EffectiveEngineVersion6')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            WorkGroupSummaryBuilder::init()
                ->name('Name4')
                ->state(WorkGroupState1::ENABLED)
                ->description('Description0')
                ->creationTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->engineVersion(
                    EngineVersion1Builder::init()
                        ->selectedEngineVersion('SelectedEngineVersion4')
                        ->effectiveEngineVersion('EffectiveEngineVersion6')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->nextToken('NextToken2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



