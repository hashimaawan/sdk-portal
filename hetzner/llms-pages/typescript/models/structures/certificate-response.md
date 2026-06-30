# Certificate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkNlcnRpZmljYXRlUmVzcG9uc2U


# Interface Name

`CertificateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate` | [`Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/certificate.md) | Required | - |


# Example

```ts
import {
  CertificateResponse,
  IssuanceEnum,
  RenewalEnum,
  TypeEnum,
} from 'hetzner-cloud-apilib';

const certificateResponse: CertificateResponse = {
  certificate: {
    certificate: '-----BEGIN CERTIFICATE-----\n...',
    created: '2016-01-30T23:55:00+00:00',
    domainNames: [
      'example.com',
      'webmail.example.com',
      'www.example.com'
    ],
    fingerprint: '03:c7:55:9b:2a:d1:04:17:09:f6:d0:7f:18:34:63:d4:3e:5f',
    id: 42,
    labels: {
      'key0': 'labels8',
      'key1': 'labels7',
      'key2': 'labels6'
    },
    name: 'my-resource',
    notValidAfter: '2019-07-08T09:59:59+00:00',
    notValidBefore: '2019-01-08T10:00:00+00:00',
    usedBy: [
      {
        id: 4711,
        type: 'load_balancer',
      }
    ],
    status: {
      error: null,
      issuance: IssuanceEnum.Completed,
      renewal: RenewalEnum.Failed,
    },
    type: TypeEnum.Uploaded,
  },
};
```



