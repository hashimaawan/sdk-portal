# V2 Certificates Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBDZXJ0aWZpY2F0ZXMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2CertificatesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate` | [`Certificate \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/certificate.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2CertificatesResponse1 } from 'digitalocean-apilib';

const v2CertificatesResponse1: V2CertificatesResponse1 = {
  certificate: {
    createdAt: '2016-03-13T12:52:32.123Z',
    dnsNames: [
      'dns_names8',
      'dns_names9',
      'dns_names0'
    ],
    id: '00002190-0000-0000-0000-000000000000',
    name: 'name2',
    notAfter: '2016-03-13T12:52:32.123Z',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



