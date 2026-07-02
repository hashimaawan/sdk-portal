# Engine Version

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkVuZ2luZVZlcnNpb24

The Athena engine version for running queries, or the PySpark engine version for running sessions.


# Class Name

`EngineVersion`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `selectedEngineVersion` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getSelectedEngineVersion(): ?string | setSelectedEngineVersion(?string selectedEngineVersion): void |
| `effectiveEngineVersion` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getEffectiveEngineVersion(): ?string | setEffectiveEngineVersion(?string effectiveEngineVersion): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\EngineVersionBuilder;

$engineVersion = EngineVersionBuilder::init()
    ->selectedEngineVersion('SelectedEngineVersion0')
    ->effectiveEngineVersion('EffectiveEngineVersion0')
    ->build();
```



