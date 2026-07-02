# Progress 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlByb2dyZXNzMg

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Progress2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `steps` | [`StepsOfAnAlertSProgress[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/steps-of-an-alert-s-progress.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Progress2, Status2 } from 'digitalocean-apilib';

const progress2: Progress2 = {
  steps: [
    {
      endedAt: '2016-03-13T12:52:32.123Z',
      name: 'name2',
      reason: {
        code: 'code2',
        message: 'message4',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      startedAt: '2016-03-13T12:52:32.123Z',
      status: Status2.Success,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      endedAt: '2016-03-13T12:52:32.123Z',
      name: 'name2',
      reason: {
        code: 'code2',
        message: 'message4',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      startedAt: '2016-03-13T12:52:32.123Z',
      status: Status2.Success,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



