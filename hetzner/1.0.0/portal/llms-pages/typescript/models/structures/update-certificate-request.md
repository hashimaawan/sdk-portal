# Update Certificate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZUNlcnRpZmljYXRlUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`UpdateCertificateRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New Certificate name |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { UpdateCertificateRequest } from 'hetzner-cloud-apilib';

const updateCertificateRequest: UpdateCertificateRequest = {
  labels: { 'labelkey': 'value' },
  name: 'my website cert',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



