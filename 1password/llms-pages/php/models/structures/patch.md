# Patch

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRlBhdGNo

*This model accepts additional fields of type array.*


# Class Name

`Patch`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `op` | [`string(Op)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/enumerations/op.md) | Required | - | getOp(): string | setOp(string op): void |
| `path` | `string` | Required | An RFC6901 JSON Pointer pointing to the Item document, an Item Attribute, and Item Field by Field ID, or an Item Field Attribute | getPath(): string | setPath(string path): void |
| `value` | `?array` | Optional | - | getValue(): ?array | setValue(?array value): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\PatchBuilder;
use M1PasswordConnectLib\Models\Op;
use M1PasswordConnectLib\ApiHelper;

$patch = PatchBuilder::init(
    Op::REMOVE,
    '/fields/06gnn2b95example10q91512p5/label'
)
    ->value(ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



