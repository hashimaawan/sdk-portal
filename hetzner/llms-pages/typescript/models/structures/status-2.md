# Status 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlN0YXR1czI

Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates


# Interface Name

`Status2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`Error2 \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/error-2.md) | Optional | If issuance or renewal reports `failed`, this property contains information about what happened |
| `issuance` | [`IssuanceEnum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/issuance.md) | Optional | Status of the issuance process of the Certificate |
| `renewal` | [`RenewalEnum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/renewal.md) | Optional | Status of the renewal process of the Certificate. |


# Example

```ts
import { IssuanceEnum, RenewalEnum, Status2 } from 'hetzner-cloud-apilib';

const status2: Status2 = {
  error: null,
  issuance: IssuanceEnum.Completed,
  renewal: RenewalEnum.Scheduled,
};
```



