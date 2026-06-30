# Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkNlcnRpZmljYXRl


# Interface Name

`Certificate`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate` | `string \| null` | Required | Certificate and chain in PEM format, in order so that each record directly certifies the one preceding |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `domainNames` | `string[]` | Required | Domains and subdomains covered by the Certificate |
| `fingerprint` | `string \| null` | Required | SHA256 fingerprint of the Certificate |
| `id` | `number` | Required | ID of the Resource |
| `labels` | `Record<string, string>` | Required | User-defined labels (key-value pairs) |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `notValidAfter` | `string \| null` | Required | Point in time when the Certificate stops being valid (in ISO-8601 format) |
| `notValidBefore` | `string \| null` | Required | Point in time when the Certificate becomes valid (in ISO-8601 format) |
| `status` | [`Status2 \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/status-2.md) | Optional | Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates |
| `type` | [`TypeEnum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/type.md) | Optional | Type of the Certificate |
| `usedBy` | [`UsedBy[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/used-by.md) | Required | Resources currently using the Certificate |


# Example

```ts
import {
  Certificate,
  IssuanceEnum,
  RenewalEnum,
  TypeEnum,
} from 'hetzner-cloud-apilib';

const certificate: Certificate = {
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
};
```



