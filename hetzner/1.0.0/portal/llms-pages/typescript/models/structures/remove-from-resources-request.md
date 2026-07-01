# Remove from Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlbW92ZUZyb21SZXNvdXJjZXNSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`RemoveFromResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `removeFrom` | [`FirewallRemoveFromResources[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/firewall-remove-from-resources.md) | Required | Resources the Firewall should be removed from |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { RemoveFromResourcesRequest, Type7 } from 'hetzner-cloud-apilib';

const removeFromResourcesRequest: RemoveFromResourcesRequest = {
  removeFrom: [
    {
      labelSelector: {
        selector: 'selector8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      server: {
        id: 14,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      type: Type7.Server,
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



