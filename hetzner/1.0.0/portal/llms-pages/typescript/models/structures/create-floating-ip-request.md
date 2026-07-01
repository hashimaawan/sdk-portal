# Create Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZUZsb2F0aW5nSVBSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`CreateFloatingIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string \| undefined` | Optional | - |
| `homeLocation` | `string \| undefined` | Optional | Home Location (routing is optimized for that Location). Only optional if Server argument is passed. |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | - |
| `server` | `number \| undefined` | Optional | Server to assign the Floating IP to |
| `type` | [`Type17`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-17.md) | Required | Floating IP type |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CreateFloatingIpRequest, Type17 } from 'hetzner-cloud-apilib';

const createFloatingIpRequest: CreateFloatingIpRequest = {
  type: Type17.Ipv4,
  description: 'Web Frontend',
  homeLocation: 'fsn1',
  labels: { 'labelkey': 'value' },
  name: 'Web Frontend',
  server: 42,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



