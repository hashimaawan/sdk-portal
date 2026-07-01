# Update Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZVByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`UpdatePrimaryIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autoDelete` | `boolean \| undefined` | Optional | Delete this Primary IP when the resource it is assigned to is deleted |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New unique name to set |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { UpdatePrimaryIpRequest } from 'hetzner-cloud-apilib';

const updatePrimaryIpRequest: UpdatePrimaryIpRequest = {
  autoDelete: true,
  labels: { 'labelkey': 'value' },
  name: 'my-ip',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



