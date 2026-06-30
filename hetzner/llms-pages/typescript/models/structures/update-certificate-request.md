# Update Certificate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZUNlcnRpZmljYXRlUmVxdWVzdA


# Interface Name

`UpdateCertificateRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New Certificate name |


# Example

```ts
import { UpdateCertificateRequest } from 'hetzner-cloud-apilib';

const updateCertificateRequest: UpdateCertificateRequest = {
  labels: { 'labelkey': 'value' },
  name: 'my website cert',
};
```



