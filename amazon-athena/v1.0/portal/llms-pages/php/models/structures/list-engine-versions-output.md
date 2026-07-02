# List Engine Versions Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc091dHB1dA


# Class Name

`ListEngineVersionsOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `engineVersions` | [`?(EngineVersion[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/engine-version.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10` | getEngineVersions(): ?array | setEngineVersions(?array engineVersions): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListEngineVersionsOutputBuilder;
use AmazonAthenaLib\Models\Builders\EngineVersionBuilder;

$listEngineVersionsOutput = ListEngineVersionsOutputBuilder::init()
    ->engineVersions(
        [
            EngineVersionBuilder::init()
                ->selectedEngineVersion('SelectedEngineVersion2')
                ->effectiveEngineVersion('EffectiveEngineVersion2')
                ->build()
        ]
    )
    ->nextToken('NextToken0')
    ->build();
```



