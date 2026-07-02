# Alert

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkFsZXJ0

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Alert`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `disabled` | `TrueClass \| FalseClass` | Optional | Is the alert disabled? |
| `operator` | [`Operator`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/operator.md) | Optional | **Default**: `Operator::UNSPECIFIED_OPERATOR` |
| `rule` | [`Rule`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/rule.md) | Optional | **Default**: `Rule::UNSPECIFIED_RULE` |
| `value` | `Float` | Optional | Threshold value for alert |
| `window` | [`Window`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/window.md) | Optional | **Default**: `Window::UNSPECIFIED_WINDOW` |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
alert = Alert.new(
  disabled: false,
  operator: Operator::GREATER_THAN,
  rule: Rule::CPU_UTILIZATION,
  value: 2.32,
  window: Window::FIVE_MINUTES,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



