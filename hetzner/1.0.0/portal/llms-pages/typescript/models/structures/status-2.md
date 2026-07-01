# Status 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXR1czI

Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates

*This model accepts additional fields of type unknown.*


# Interface Name

`Status2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`Error2 \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/error-2.md) | Optional | If issuance or renewal reports `failed`, this property contains information about what happened |
| `issuance` | [`Issuance \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/issuance.md) | Optional | Status of the issuance process of the Certificate |
| `renewal` | [`Renewal \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/renewal.md) | Optional | Status of the renewal process of the Certificate. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Issuance, Renewal, Status2 } from 'hetzner-cloud-apilib';

const status2: Status2 = {
  error: null,
  issuance: Issuance.Completed,
  renewal: Renewal.Scheduled,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



