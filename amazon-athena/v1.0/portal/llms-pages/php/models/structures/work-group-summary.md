# Work Group Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRldvcmtHcm91cFN1bW1hcnk

The summary information for the workgroup, which includes its name, state, description, and the date and time it was created.

*This model accepts additional fields of type array.*


# Class Name

`WorkGroupSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getName(): ?string | setName(?string name): void |
| `state` | [`?string(WorkGroupState1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/work-group-state-1.md) | Optional | - | getState(): ?string | setState(?string state): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `creationTime` | `?DateTime` | Optional | - | getCreationTime(): ?\DateTime | setCreationTime(?\DateTime creationTime): void |
| `engineVersion` | [`?EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/engine-version-1.md) | Optional | - | getEngineVersion(): ?EngineVersion1 | setEngineVersion(?EngineVersion1 engineVersion): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\WorkGroupSummaryBuilder;
use AmazonAthenaLib\Models\WorkGroupState1;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\Builders\EngineVersion1Builder;
use AmazonAthenaLib\ApiHelper;

$workGroupSummary = WorkGroupSummaryBuilder::init()
    ->name('Name4')
    ->state(WorkGroupState1::ENABLED)
    ->description('Description8')
    ->creationTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->engineVersion(
        EngineVersion1Builder::init()
            ->selectedEngineVersion('SelectedEngineVersion4')
            ->effectiveEngineVersion('EffectiveEngineVersion6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



