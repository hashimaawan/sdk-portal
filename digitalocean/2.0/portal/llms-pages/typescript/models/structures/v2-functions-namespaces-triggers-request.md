# V2 Functions Namespaces Triggers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2FunctionsNamespacesTriggersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mFunction` | `string` | Required | Name of function(action) that exists in the given namespace. |
| `isEnabled` | `boolean` | Required | Indicates weather the trigger is paused or unpaused. |
| `name` | `string` | Required | The trigger's unique name within the namespace. |
| `scheduledDetails` | [`ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/scheduled-details.md) | Required | Trigger details for SCHEDULED type, where body is optional. |
| `type` | `string` | Required | One of different type of triggers. Currently only SCHEDULED is supported. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2FunctionsNamespacesTriggersRequest } from 'digitalocean-apilib';

const v2FunctionsNamespacesTriggersRequest: V2FunctionsNamespacesTriggersRequest = {
  mFunction: 'hello',
  isEnabled: true,
  name: 'my trigger',
  scheduledDetails: {
    cron: '* * * * *',
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
  type: 'SCHEDULED',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



