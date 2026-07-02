# Alert

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkFsZXJ0

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Alert`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `disabled` | `?bool` | Optional | Is the alert disabled? | getDisabled(): ?bool | setDisabled(?bool disabled): void |
| `operator` | [`?string(Operator)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/operator.md) | Optional | **Default**: `Operator::UNSPECIFIED_OPERATOR` | getOperator(): ?string | setOperator(?string operator): void |
| `rule` | [`?string(Rule)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/rule.md) | Optional | **Default**: `Rule::UNSPECIFIED_RULE` | getRule(): ?string | setRule(?string rule): void |
| `value` | `?float` | Optional | Threshold value for alert | getValue(): ?float | setValue(?float value): void |
| `window` | [`?string(Window)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/window.md) | Optional | **Default**: `Window::UNSPECIFIED_WINDOW` | getWindow(): ?string | setWindow(?string window): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\AlertBuilder;
use DigitalOceanApiLib\Models\Operator;
use DigitalOceanApiLib\Models\Rule;
use DigitalOceanApiLib\Models\Window;
use DigitalOceanApiLib\ApiHelper;

$alert = AlertBuilder::init()
    ->disabled(false)
    ->operator(Operator::GREATER_THAN)
    ->rule(Rule::CPU_UTILIZATION)
    ->value(2.32)
    ->window(Window::FIVE_MINUTES)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



