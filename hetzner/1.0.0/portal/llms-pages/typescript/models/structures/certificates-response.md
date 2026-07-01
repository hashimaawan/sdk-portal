# Certificates Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNlcnRpZmljYXRlc1Jlc3BvbnNl

*This model accepts additional fields of type unknown.*


# Interface Name

`CertificatesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificates` | [`Certificate[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/certificate.md) | Required | - |
| `meta` | [`Meta \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/meta.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CertificatesResponse,
  Issuance,
  Renewal,
  Type,
} from 'hetzner-cloud-apilib';

const certificatesResponse: CertificatesResponse = {
  certificates: [
    {
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
        'key0': 'labels2',
        'key1': 'labels1',
        'key2': 'labels0'
      },
      name: 'my-resource',
      notValidAfter: '2019-07-08T09:59:59+00:00',
      notValidBefore: '2019-01-08T10:00:00+00:00',
      usedBy: [
        {
          id: 4711,
          type: 'load_balancer',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      status: {
        error: null,
        issuance: Issuance.Completed,
        renewal: Renewal.Failed,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      type: Type.Uploaded,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  meta: {
    pagination: {
      lastPage: 77.7,
      nextPage: 209.18,
      page: 17.58,
      perPage: 13.34,
      previousPage: 50.02,
      totalEntries: 206.64,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



