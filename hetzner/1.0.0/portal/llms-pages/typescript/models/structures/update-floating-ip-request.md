# Update Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZUZsb2F0aW5nSVBSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`UpdateFloatingIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string \| undefined` | Optional | New Description to set |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New unique name to set |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { UpdateFloatingIpRequest } from 'hetzner-cloud-apilib';

const updateFloatingIpRequest: UpdateFloatingIpRequest = {
  description: 'Web Frontend',
  labels: { 'labelkey': 'value' },
  name: 'Web Frontend',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



