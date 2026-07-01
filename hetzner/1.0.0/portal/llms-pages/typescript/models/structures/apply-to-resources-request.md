# Apply to Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkFwcGx5VG9SZXNvdXJjZXNSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`ApplyToResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applyTo` | [`FirewallApplyToResources[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/firewall-apply-to-resources.md) | Required | Resources the Firewall should be applied to |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ApplyToResourcesRequest, Type7 } from 'hetzner-cloud-apilib';

const applyToResourcesRequest: ApplyToResourcesRequest = {
  applyTo: [
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



