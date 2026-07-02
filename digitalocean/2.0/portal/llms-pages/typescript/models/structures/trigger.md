# Trigger

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlRyaWdnZXI

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Trigger`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional | UTC time string. |
| `mFunction` | `string \| undefined` | Optional | Name of function(action) that exists in the given namespace. |
| `isEnabled` | `boolean \| undefined` | Optional | Indicates weather the trigger is paused or unpaused. |
| `name` | `string \| undefined` | Optional | The trigger's unique name within the namespace. |
| `namespace` | `string \| undefined` | Optional | A unique string format of UUID with a prefix fn-. |
| `scheduledDetails` | [`ScheduledDetails \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/scheduled-details.md) | Optional | Trigger details for SCHEDULED type, where body is optional. |
| `scheduledRuns` | [`ScheduledRuns \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/scheduled-runs.md) | Optional | - |
| `type` | `string \| undefined` | Optional | String which indicates the type of trigger source like SCHEDULED. |
| `updatedAt` | `string \| undefined` | Optional | UTC time string. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Trigger } from 'digitalocean-apilib';

const trigger: Trigger = {
  createdAt: '2022-11-11T04:16:45Z',
  mFunction: 'hello',
  isEnabled: true,
  name: 'my trigger',
  namespace: 'fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx',
  type: 'SCHEDULED',
  updatedAt: '2022-11-11T04:16:45Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



