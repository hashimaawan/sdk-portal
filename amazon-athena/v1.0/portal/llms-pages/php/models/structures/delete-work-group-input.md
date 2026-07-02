# Delete Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkRlbGV0ZVdvcmtHcm91cElucHV0


# Class Name

`DeleteWorkGroupInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): string | setWorkGroup(string workGroup): void |
| `recursiveDeleteOption` | `?bool` | Optional | - | getRecursiveDeleteOption(): ?bool | setRecursiveDeleteOption(?bool recursiveDeleteOption): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\DeleteWorkGroupInputBuilder;

$deleteWorkGroupInput = DeleteWorkGroupInputBuilder::init(
    'WorkGroup0'
)
    ->recursiveDeleteOption(false)
    ->build();
```



