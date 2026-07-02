# Contains All Domains for the App

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkNvbnRhaW5zJTI1MjBhbGwlMjUyMGRvbWFpbnMlMjUyMGZvciUyNTIwdGhlJTI1MjBhcHA

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`ContainsAllDomainsForTheApp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificateExpiresAt` | `string \| undefined` | Optional, Read-only | - |
| `id` | `string \| undefined` | Optional | - |
| `phase` | [`Phase1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/phase-1.md) | Optional | **Default**: `Phase1.Unknown` |
| `progress` | [`Progress1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/progress-1.md) | Optional | - |
| `rotateValidationRecords` | `boolean \| undefined` | Optional, Read-only | - |
| `spec` | [`Domain \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/domain.md) | Optional | - |
| `validations` | [`ListOfTxtValidationRecord[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/list-of-txt-validation-record.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { ContainsAllDomainsForTheApp, Phase1 } from 'digitalocean-apilib';

const containsAllDomainsForTheApp: ContainsAllDomainsForTheApp = {
  certificateExpiresAt: '2024-01-29T23:59:59Z',
  id: '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
  phase: Phase1.Active,
  progress: {
    steps: [
      { 'key1': 'val1', 'key2': 'val2' },
      { 'key1': 'val1', 'key2': 'val2' },
      { 'key1': 'val1', 'key2': 'val2' }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  rotateValidationRecords: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



