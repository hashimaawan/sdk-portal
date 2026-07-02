# List Application DPU Sizes Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzT3V0cHV0


# Class Name

`ListApplicationDPUSizesOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `applicationDPUSizes` | [`?(ApplicationDPUSizes[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/application-dpu-sizes.md) | Optional | - | getApplicationDPUSizes(): ?array | setApplicationDPUSizes(?array applicationDPUSizes): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListApplicationDPUSizesOutputBuilder;
use AmazonAthenaLib\Models\Builders\ApplicationDPUSizesBuilder;

$listApplicationDPUSizesOutput = ListApplicationDPUSizesOutputBuilder::init()
    ->applicationDPUSizes(
        [
            ApplicationDPUSizesBuilder::init()
                ->applicationRuntimeId('ApplicationRuntimeId0')
                ->supportedDPUSizes(
                    [
                        113,
                        114
                    ]
                )
                ->build(),
            ApplicationDPUSizesBuilder::init()
                ->applicationRuntimeId('ApplicationRuntimeId0')
                ->supportedDPUSizes(
                    [
                        113,
                        114
                    ]
                )
                ->build()
        ]
    )
    ->nextToken('NextToken0')
    ->build();
```



