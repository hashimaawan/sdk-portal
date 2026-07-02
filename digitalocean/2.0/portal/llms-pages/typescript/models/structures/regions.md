# Regions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlZ2lvbnM

A map of region to regional state

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Regions`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `euWest` | [`EuWest \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/eu-west.md) | Optional | - |
| `usEast` | [`EuWest \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/eu-west.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Regions, Status16 } from 'digitalocean-apilib';

const regions: Regions = {
  euWest: {
    status: Status16.Down,
    statusChangedAt: 'status_changed_at4',
    thirtyDayUptimePercentage: 227.78,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  usEast: {
    status: Status16.Down,
    statusChangedAt: 'status_changed_at4',
    thirtyDayUptimePercentage: 121.56,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



