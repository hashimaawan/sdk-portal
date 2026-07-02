# Steps of an Alert S Progress

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0ZXBzJTI1MjBvZiUyNTIwYW4lMjUyMGFsZXJ0JTI1MjdzJTI1MjBwcm9ncmVzcy4

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`StepsOfAnAlertSProgress`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `endedAt` | `string \| undefined` | Optional | - |
| `name` | `string \| undefined` | Optional | - |
| `reason` | [`Reason \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/reason.md) | Optional | - |
| `startedAt` | `string \| undefined` | Optional | - |
| `status` | [`Status2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status-2.md) | Optional | **Default**: `Status2.Unknown` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Status2, StepsOfAnAlertSProgress } from 'digitalocean-apilib';

const stepsOfAnAlertSProgress: StepsOfAnAlertSProgress = {
  endedAt: '2020-11-19T20:27:18Z',
  name: 'example_step',
  reason: {
    code: 'code2',
    message: 'message4',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  startedAt: '2020-11-19T20:27:18Z',
  status: Status2.Success,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



