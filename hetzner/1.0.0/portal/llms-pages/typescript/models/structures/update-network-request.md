# Update Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZU5ldHdvcmtSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`UpdateNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | [`Labels2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New network name |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { UpdateNetworkRequest } from 'hetzner-cloud-apilib';

const updateNetworkRequest: UpdateNetworkRequest = {
  labels: {
    labelkey: 'labelkey4',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  name: 'new-name',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



