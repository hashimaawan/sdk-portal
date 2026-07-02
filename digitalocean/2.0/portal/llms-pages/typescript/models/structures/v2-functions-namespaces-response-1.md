# V2 Functions Namespaces Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2FunctionsNamespacesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `namespace` | [`Namespace \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/namespace.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2FunctionsNamespacesResponse1 } from 'digitalocean-apilib';

const v2FunctionsNamespacesResponse1: V2FunctionsNamespacesResponse1 = {
  namespace: {
    apiHost: 'api_host2',
    createdAt: 'created_at0',
    key: 'key2',
    label: 'label2',
    namespace: 'namespace0',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



