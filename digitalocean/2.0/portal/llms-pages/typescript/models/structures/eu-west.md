# Eu West

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkV1V2VzdA

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`EuWest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`Status16 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status-16.md) | Optional | - |
| `statusChangedAt` | `string \| undefined` | Optional | - |
| `thirtyDayUptimePercentage` | `number \| undefined` | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { EuWest, Status16 } from 'digitalocean-apilib';

const euWest: EuWest = {
  status: Status16.Up,
  statusChangedAt: '2022-03-17T22:28:51Z',
  thirtyDayUptimePercentage: 97.99,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



