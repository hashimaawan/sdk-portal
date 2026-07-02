# Alert

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkFsZXJ0

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Alert`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `disabled` | `boolean \| undefined` | Optional | Is the alert disabled? |
| `operator` | [`Operator \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/operator.md) | Optional | **Default**: `Operator.UnspecifiedOperator` |
| `rule` | [`Rule \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/rule.md) | Optional | **Default**: `Rule.UnspecifiedRule` |
| `value` | `number \| undefined` | Optional | Threshold value for alert |
| `window` | [`Window \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/window.md) | Optional | **Default**: `Window.UnspecifiedWindow` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Alert, Operator, Rule, Window } from 'digitalocean-apilib';

const alert: Alert = {
  disabled: false,
  operator: Operator.GreaterThan,
  rule: Rule.CpuUtilization,
  value: 2.32,
  window: Window.FiveMinutes,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



