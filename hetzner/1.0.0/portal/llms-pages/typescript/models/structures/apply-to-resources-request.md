# Apply to Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkFwcGx5VG9SZXNvdXJjZXNSZXF1ZXN0


# Interface Name

`ApplyToResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applyTo` | [`FirewallApplyToResources[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/firewall-apply-to-resources.md) | Required | Resources the Firewall should be applied to |


# Example

```ts
import { ApplyToResourcesRequest, Type7Enum } from 'hetzner-cloud-apilib';

const applyToResourcesRequest: ApplyToResourcesRequest = {
  applyTo: [
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



