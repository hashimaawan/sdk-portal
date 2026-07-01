# Create Certificate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZUNlcnRpZmljYXRlUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`CreateCertificateRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate` | `string \| undefined` | Optional | Certificate and chain in PEM format, in order so that each record directly certifies the one preceding. Required for type `uploaded` Certificates. |
| `domainNames` | `string[] \| undefined` | Optional | Domains and subdomains that should be contained in the Certificate issued by *Let's Encrypt*. Required for type `managed` Certificates. |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string` | Required | Name of the Certificate |
| `privateKey` | `string \| undefined` | Optional | Certificate key in PEM format. Required for type `uploaded` Certificates. |
| `type` | [`Type1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-1.md) | Optional | Choose between uploading a Certificate in PEM format or requesting a managed *Let's Encrypt* Certificate. If omitted defaults to `uploaded`. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CreateCertificateRequest, Type1 } from 'hetzner-cloud-apilib';

const createCertificateRequest: CreateCertificateRequest = {
  name: 'my website cert',
  certificate: '-----BEGIN CERTIFICATE-----\n...',
  domainNames: [
    'domain_names8',
    'domain_names9',
    'domain_names0'
  ],
  labels: { 'key1': 'val1', 'key2': 'val2' },
  privateKey: '-----BEGIN PRIVATE KEY-----\n...',
  type: Type1.Uploaded,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



