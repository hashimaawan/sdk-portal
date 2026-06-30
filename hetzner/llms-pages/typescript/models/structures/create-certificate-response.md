# Create Certificate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZUNlcnRpZmljYXRlUmVzcG9uc2U


# Interface Name

`CreateCertificateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`NullableAction \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/nullable-action.md) | Optional | - |
| `certificate` | [`Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/certificate.md) | Required | - |


# Example

```ts
import {
  CreateCertificateResponse,
  IssuanceEnum,
  RenewalEnum,
  StatusEnum,
  TypeEnum,
} from 'hetzner-cloud-apilib';

const createCertificateResponse: CreateCertificateResponse = {
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
  action: {
    command: 'command6',
    error: {
      code: 'code2',
      message: 'message4',
    },
    finished: 'finished0',
    id: 238,
    progress: 143.26,
    resources: [
      {
        id: 198,
        type: 'type0',
      },
      {
        id: 198,
        type: 'type0',
      },
      {
        id: 198,
        type: 'type0',
      }
    ],
    started: 'started8',
    status: StatusEnum.Running,
  },
};
```



