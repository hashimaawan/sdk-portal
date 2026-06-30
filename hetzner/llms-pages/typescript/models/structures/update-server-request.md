# Update Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZVNlcnZlclJlcXVlc3Q


# Interface Name

`UpdateServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New name to set |


# Example

```ts
import { UpdateServerRequest } from 'hetzner-cloud-apilib';

const updateServerRequest: UpdateServerRequest = {
  labels: { 'labelkey': 'value' },
  name: 'my-server',
};
```



