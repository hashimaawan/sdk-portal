# Update Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZUZpcmV3YWxsUmVxdWVzdA


# Interface Name

`UpdateFirewallRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New Firewall name |


# Example

```ts
import { UpdateFirewallRequest } from 'hetzner-cloud-apilib';

const updateFirewallRequest: UpdateFirewallRequest = {
  labels: { 'labelkey': 'value' },
  name: 'new-name',
};
```



