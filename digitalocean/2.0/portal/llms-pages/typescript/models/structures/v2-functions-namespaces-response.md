# V2 Functions Namespaces Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2FunctionsNamespacesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `namespaces` | [`Namespace[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/namespace.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2FunctionsNamespacesResponse } from 'digitalocean-apilib';

const v2FunctionsNamespacesResponse: V2FunctionsNamespacesResponse = {
  namespaces: [
    {
      apiHost: 'api_host8',
      createdAt: 'created_at0',
      key: 'key2',
      label: 'label2',
      namespace: 'namespace0',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      apiHost: 'api_host8',
      createdAt: 'created_at0',
      key: 'key2',
      label: 'label2',
      namespace: 'namespace0',
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



