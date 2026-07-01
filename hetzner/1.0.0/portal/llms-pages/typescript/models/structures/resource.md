# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc291cmNl


# Interface Name

`Resource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Required | ID of the Resource |
| `type` | `string` | Required | Type of resource referenced |


# Example

```ts
import { Resource } from 'hetzner-cloud-apilib';

const resource: Resource = {
  id: 42,
  type: 'server',
};
```



