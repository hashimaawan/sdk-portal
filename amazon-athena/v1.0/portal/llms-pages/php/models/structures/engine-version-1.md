# Engine Version 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkVuZ2luZVZlcnNpb24x

*This model accepts additional fields of type array.*


# Class Name

`EngineVersion1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `selectedEngineVersion` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getSelectedEngineVersion(): ?string | setSelectedEngineVersion(?string selectedEngineVersion): void |
| `effectiveEngineVersion` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getEffectiveEngineVersion(): ?string | setEffectiveEngineVersion(?string effectiveEngineVersion): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\EngineVersion1Builder;
use AmazonAthenaLib\ApiHelper;

$engineVersion1 = EngineVersion1Builder::init()
    ->selectedEngineVersion('SelectedEngineVersion2')
    ->effectiveEngineVersion('EffectiveEngineVersion8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



