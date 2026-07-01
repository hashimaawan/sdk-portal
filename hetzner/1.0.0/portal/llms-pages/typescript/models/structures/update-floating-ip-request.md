# Update Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZUZsb2F0aW5nSVBSZXF1ZXN0


# Interface Name

`UpdateFloatingIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string \| undefined` | Optional | New Description to set |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New unique name to set |


# Example

```ts
import { UpdateFloatingIPRequest } from 'hetzner-cloud-apilib';

const updateFloatingIPRequest: UpdateFloatingIPRequest = {
  description: 'Web Frontend',
  labels: { 'labelkey': 'value' },
  name: 'Web Frontend',
};
```



