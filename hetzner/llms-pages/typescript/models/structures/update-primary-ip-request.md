# Update Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZVByaW1hcnlJUFJlcXVlc3Q


# Interface Name

`UpdatePrimaryIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autoDelete` | `boolean \| undefined` | Optional | Delete this Primary IP when the resource it is assigned to is deleted |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New unique name to set |


# Example

```ts
import { UpdatePrimaryIPRequest } from 'hetzner-cloud-apilib';

const updatePrimaryIPRequest: UpdatePrimaryIPRequest = {
  autoDelete: true,
  labels: { 'labelkey': 'value' },
  name: 'my-ip',
};
```



