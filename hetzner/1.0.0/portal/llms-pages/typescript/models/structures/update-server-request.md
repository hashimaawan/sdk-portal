# Update Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZVNlcnZlclJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`UpdateServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New name to set |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { UpdateServerRequest } from 'hetzner-cloud-apilib';

const updateServerRequest: UpdateServerRequest = {
  labels: { 'labelkey': 'value' },
  name: 'my-server',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



