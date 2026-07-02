# V2 Functions Namespaces Triggers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2FunctionsNamespacesTriggersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `trigger` | [`Trigger \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/trigger.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2FunctionsNamespacesTriggersResponse1 } from 'digitalocean-apilib';

const v2FunctionsNamespacesTriggersResponse1: V2FunctionsNamespacesTriggersResponse1 = {
  trigger: {
    createdAt: 'created_at6',
    mFunction: 'function6',
    isEnabled: false,
    name: 'name8',
    namespace: 'namespace4',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



