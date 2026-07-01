# Remove from Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlbW92ZUZyb21SZXNvdXJjZXNSZXF1ZXN0


# Interface Name

`RemoveFromResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `removeFrom` | [`FirewallRemoveFromResources[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/firewall-remove-from-resources.md) | Required | Resources the Firewall should be removed from |


# Example

```ts
import { RemoveFromResourcesRequest, Type7Enum } from 'hetzner-cloud-apilib';

const removeFromResourcesRequest: RemoveFromResourcesRequest = {
  removeFrom: [
    {
      labelSelector: {
        selector: 'selector8',
      },
      server: {
        id: 14,
      },
      type: Type7Enum.Server,
    }
  ],
};
```



