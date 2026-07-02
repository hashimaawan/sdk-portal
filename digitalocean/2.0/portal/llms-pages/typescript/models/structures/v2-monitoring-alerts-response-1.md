# V2 Monitoring Alerts Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBNb25pdG9yaW5nJTI1MjBBbGVydHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2MonitoringAlertsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `policy` | [`Policy \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/policy.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Compare,
  Type17,
  V2MonitoringAlertsResponse1,
  Window1,
} from 'digitalocean-apilib';

const v2MonitoringAlertsResponse1: V2MonitoringAlertsResponse1 = {
  policy: {
    alerts: {
      email: [
        'email2',
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
    compare: Compare.GreaterThan,
    description: 'description4',
    enabled: false,
    entities: [
      'entities9'
    ],
    tags: [
      'tags9',
      'tags0',
      'tags1'
    ],
    type: Type17.EnumV1InsightsdropletdiskRead,
    uuid: 'uuid0',
    value: 149.36,
    window: Window1.Enum30M,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



