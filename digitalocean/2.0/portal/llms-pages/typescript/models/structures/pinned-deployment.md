# Pinned Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlBpbm5lZERlcGxveW1lbnQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`PinnedDeployment`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cause` | `string \| undefined` | Optional | - |
| `clonedFrom` | `string \| undefined` | Optional | - |
| `createdAt` | `string \| undefined` | Optional | - |
| `functions` | [`FunctionsComponentsThatArePartOfThisDeployment[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/functions-components-that-are-part-of-this-deployment.md) | Optional | - |
| `id` | `string \| undefined` | Optional | - |
| `jobs` | [`JobComponentsThatArePartOfThisDeployment[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/job-components-that-are-part-of-this-deployment.md) | Optional | - |
| `phase` | [`Phase \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/phase.md) | Optional | **Default**: `Phase.Unknown` |
| `phaseLastUpdatedAt` | `string \| undefined` | Optional | - |
| `progress` | [`Progress \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/progress.md) | Optional | - |
| `services` | [`ServiceComponentsThatArePartOfThisDeployment[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/service-components-that-are-part-of-this-deployment.md) | Optional | - |
| `spec` | [`AppSpec \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/app-spec.md) | Optional | The desired configuration of an application. |
| `staticSites` | [`StaticSiteComponentsThatArePartOfThisDeployment[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/static-site-components-that-are-part-of-this-deployment.md) | Optional | - |
| `tierSlug` | `string \| undefined` | Optional, Read-only | - |
| `updatedAt` | `string \| undefined` | Optional | - |
| `workers` | [`WorkerComponentsThatArePartOfThisDeployment[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/worker-components-that-are-part-of-this-deployment.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Phase, PinnedDeployment } from 'digitalocean-apilib';

const pinnedDeployment: PinnedDeployment = {
  cause: 'commit 9a4df0b pushed to github/digitalocean/sample-golang',
  clonedFrom: '3aa4d20e-5527-4c00-b496-601fbd22520a',
  createdAt: '2020-07-28T18:00:00Z',
  functions: [
    {
      name: 'name4',
      namespace: 'namespace8',
      sourceCommitHash: 'source_commit_hash4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      name: 'name4',
      namespace: 'namespace8',
      sourceCommitHash: 'source_commit_hash4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      name: 'name4',
      namespace: 'namespace8',
      sourceCommitHash: 'source_commit_hash4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  id: 'b6bdf840-2854-4f87-a36c-5f231c617c84',
  phase: Phase.Active,
  phaseLastUpdatedAt: '0001-01-01T00:00:00Z',
  tierSlug: 'basic',
  updatedAt: '2020-07-28T18:00:00Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



