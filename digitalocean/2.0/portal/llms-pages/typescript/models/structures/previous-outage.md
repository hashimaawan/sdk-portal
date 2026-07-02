# Previous Outage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlByZXZpb3VzT3V0YWdl

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`PreviousOutage`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `durationSeconds` | `number \| undefined` | Optional | - |
| `endedAt` | `string \| undefined` | Optional | - |
| `region` | `string \| undefined` | Optional | - |
| `startedAt` | `string \| undefined` | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { PreviousOutage } from 'digitalocean-apilib';

const previousOutage: PreviousOutage = {
  durationSeconds: 120,
  endedAt: '2022-03-17T18:06:55Z',
  region: 'us_east',
  startedAt: '2022-03-17T18:04:55Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



