# A Step that Is Run as Part of the Deployment S Lifecycle

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkElMjUyMHN0ZXAlMjUyMHRoYXQlMjUyMGlzJTI1MjBydW4lMjUyMGFzJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhlJTI1MjBkZXBsb3ltZW50JTI1MjdzJTI1MjBsaWZlY3ljbGU

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`AStepThatIsRunAsPartOfTheDeploymentSLifecycle`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `componentName` | `string \| undefined` | Optional | - |
| `endedAt` | `string \| undefined` | Optional | - |
| `messageBase` | `string \| undefined` | Optional | The base of a human-readable description of the step intended to be combined with the component name for presentation. For example:<br><br>`message_base` = "Building service"<br>`component_name` = "api" |
| `name` | `string \| undefined` | Optional | - |
| `reason` | [`Reason \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/reason.md) | Optional | - |
| `startedAt` | `string \| undefined` | Optional | - |
| `status` | [`Status2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status-2.md) | Optional | **Default**: `Status2.Unknown` |
| `steps` | [`unknown[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  AStepThatIsRunAsPartOfTheDeploymentSLifecycle,
  Status2,
} from 'digitalocean-apilib';

const aStepThatIsRunAsPartOfTheDeploymentSLifecycle: AStepThatIsRunAsPartOfTheDeploymentSLifecycle = {
  componentName: 'component',
  endedAt: '2020-11-19T20:27:18Z',
  messageBase: 'Building service',
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



