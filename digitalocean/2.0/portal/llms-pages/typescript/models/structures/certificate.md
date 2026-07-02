# Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkNlcnRpZmljYXRl

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Certificate`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the certificate was created. |
| `dnsNames` | `string[] \| undefined` | Optional | An array of fully qualified domain names (FQDNs) for which the certificate was issued. |
| `id` | `string \| undefined` | Optional, Read-only | A unique ID that can be used to identify and reference a certificate. |
| `name` | `string \| undefined` | Optional | A unique human-readable name referring to a certificate. |
| `notAfter` | `string \| undefined` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents the certificate's expiration date. |
| `sha1Fingerprint` | `string \| undefined` | Optional, Read-only | A unique identifier generated from the SHA-1 fingerprint of the certificate. |
| `state` | [`State \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/state.md) | Optional, Read-only | A string representing the current state of the certificate. It may be `pending`, `verified`, or `error`. |
| `type` | [`Type4 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/type-4.md) | Optional | A string representing the type of the certificate. The value will be `custom` for a user-uploaded certificate or `lets_encrypt` for one automatically generated with Let's Encrypt. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Certificate, State, Type4 } from 'digitalocean-apilib';

const certificate: Certificate = {
  createdAt: '2017-02-08T16:02:37Z',
  dnsNames: [
    'www.example.com',
    'example.com'
  ],
  id: '892071a0-bb95-49bc-8021-3afd67a210bf',
  name: 'web-cert-01',
  notAfter: '2017-02-22T00:23:00Z',
  sha1Fingerprint: 'dfcc9f57d86bf58e321c2c6c31c7a971be244ac7',
  state: State.Verified,
  type: Type4.LetsEncrypt,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



