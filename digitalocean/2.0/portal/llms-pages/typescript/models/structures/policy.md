# Policy

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlBvbGljeQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Policy`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alerts` | [`Alerts`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/alerts.md) | Required | - |
| `compare` | [`Compare`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/compare.md) | Required | - |
| `description` | `string` | Required | - |
| `enabled` | `boolean` | Required | - |
| `entities` | `string[]` | Required | - |
| `tags` | `string[]` | Required | - |
| `type` | [`Type17`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/type-17.md) | Required | - |
| `uuid` | `string` | Required | - |
| `value` | `number` | Required | - |
| `window` | [`Window1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/window-1.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Compare, Policy, Type17, Window1 } from 'digitalocean-apilib';

const policy: Policy = {
  alerts: {
    email: [
      'bob@exmaple.com'
    ],
    slack: [
      {
        channel: 'Production Alerts',
        url: 'https://hooks.slack.com/services/T1234567/AAAAAAAA/ZZZZZZ',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  compare: Compare.GreaterThan,
  description: 'CPU Alert',
  enabled: true,
  entities: [
    '192018292'
  ],
  tags: [
    'droplet_tag'
  ],
  type: Type17.EnumV1Insightsdropletcpu,
  uuid: '78b3da62-27e5-49ba-ac70-5db0b5935c64',
  value: 80,
  window: Window1.Enum5M,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



