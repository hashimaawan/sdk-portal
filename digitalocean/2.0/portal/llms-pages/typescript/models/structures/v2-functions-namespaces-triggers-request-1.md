# V2 Functions Namespaces Triggers Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2FunctionsNamespacesTriggersRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `isEnabled` | `boolean \| undefined` | Optional | Indicates weather the trigger is paused or unpaused. |
| `scheduledDetails` | [`ScheduledDetails \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/scheduled-details.md) | Optional | Trigger details for SCHEDULED type, where body is optional. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2FunctionsNamespacesTriggersRequest1 } from 'digitalocean-apilib';

const v2FunctionsNamespacesTriggersRequest1: V2FunctionsNamespacesTriggersRequest1 = {
  isEnabled: true,
  scheduledDetails: {
    cron: 'cron2',
    body: {
      name: 'name6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



