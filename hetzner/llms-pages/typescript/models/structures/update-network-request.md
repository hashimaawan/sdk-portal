# Update Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZU5ldHdvcmtSZXF1ZXN0


# Interface Name

`UpdateNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | [`Labels2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New network name |


# Example

```ts
import { UpdateNetworkRequest } from 'hetzner-cloud-apilib';

const updateNetworkRequest: UpdateNetworkRequest = {
  labels: {
    labelkey: 'labelkey4',
  },
  name: 'new-name',
};
```



