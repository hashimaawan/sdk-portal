# Progress

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlByb2dyZXNz

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Progress`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `errorSteps` | `number \| undefined` | Optional | - |
| `pendingSteps` | `number \| undefined` | Optional | - |
| `runningSteps` | `number \| undefined` | Optional | - |
| `steps` | [`AStepThatIsRunAsPartOfTheDeploymentSLifecycle[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/a-step-that-is-run-as-part-of-the-deployment-s-lifecycle.md) | Optional | - |
| `successSteps` | `number \| undefined` | Optional | - |
| `summarySteps` | [`AStepThatIsRunAsPartOfTheDeploymentSLifecycle[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/a-step-that-is-run-as-part-of-the-deployment-s-lifecycle.md) | Optional | - |
| `totalSteps` | `number \| undefined` | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Progress } from 'digitalocean-apilib';

const progress: Progress = {
  errorSteps: 3,
  pendingSteps: 2,
  runningSteps: 2,
  steps: [
    {
      componentName: 'component_name0',
      endedAt: '2016-03-13T12:52:32.123Z',
      messageBase: 'message_base4',
      name: 'name2',
      reason: {
        code: 'code2',
        message: 'message4',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      componentName: 'component_name0',
      endedAt: '2016-03-13T12:52:32.123Z',
      messageBase: 'message_base4',
      name: 'name2',
      reason: {
        code: 'code2',
        message: 'message4',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      componentName: 'component_name0',
      endedAt: '2016-03-13T12:52:32.123Z',
      messageBase: 'message_base4',
      name: 'name2',
      reason: {
        code: 'code2',
        message: 'message4',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  successSteps: 4,
  totalSteps: 5,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



