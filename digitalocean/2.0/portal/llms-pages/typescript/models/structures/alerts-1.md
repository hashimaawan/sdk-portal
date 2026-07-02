# Alerts 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkFsZXJ0czE

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Alerts1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string \| undefined` | Optional, Read-only | A unique ID that can be used to identify and reference the alert. |
| `comparison` | [`Comparison \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/comparison.md) | Optional | The comparison operator used against the alert's threshold. |
| `name` | `string \| undefined` | Optional | A human-friendly display name. |
| `notifications` | [`Notifications \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/notifications.md) | Optional | The notification settings for a trigger alert. |
| `period` | [`Period \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/period.md) | Optional | Period of time the threshold must be exceeded to trigger the alert. |
| `threshold` | `number \| undefined` | Optional | The threshold at which the alert will enter a trigger state. The specific threshold is dependent on the alert type. |
| `type` | [`Type20 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/type-20.md) | Optional | The type of alert. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Alerts1, Comparison, Period, Type20 } from 'digitalocean-apilib';

const alerts1: Alerts1 = {
  id: '5a4981aa-9653-4bd1-bef5-d6bff52042e4',
  comparison: Comparison.GreaterThan,
  name: 'Landing page degraded performance',
  notifications: {
    email: [
      'email4',
      'email3'
    ],
    slack: [
      {
        channel: 'channel6',
        url: 'url2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        channel: 'channel6',
        url: 'url2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        channel: 'channel6',
        url: 'url2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  period: Period.Enum2M,
  threshold: 300,
  type: Type20.Latency,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



