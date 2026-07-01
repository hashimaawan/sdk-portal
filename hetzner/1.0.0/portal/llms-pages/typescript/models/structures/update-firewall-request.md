# Update Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZUZpcmV3YWxsUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`UpdateFirewallRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New Firewall name |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { UpdateFirewallRequest } from 'hetzner-cloud-apilib';

const updateFirewallRequest: UpdateFirewallRequest = {
  labels: { 'labelkey': 'value' },
  name: 'new-name',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



