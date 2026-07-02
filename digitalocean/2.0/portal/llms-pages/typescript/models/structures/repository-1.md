# Repository 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlcG9zaXRvcnkx

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Repository1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `latestManifest` | [`LatestManifest \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/latest-manifest.md) | Optional | - |
| `manifestCount` | `number \| undefined` | Optional | The number of manifests in the repository. |
| `name` | `string \| undefined` | Optional | The name of the repository. |
| `registryName` | `string \| undefined` | Optional | The name of the container registry. |
| `tagCount` | `number \| undefined` | Optional | The number of tags in the repository. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Repository1 } from 'digitalocean-apilib';

const repository1: Repository1 = {
  latestManifest: {
    blobs: [
      {
        compressedSizeBytes: 12,
        digest: 'digest2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        compressedSizeBytes: 12,
        digest: 'digest2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        compressedSizeBytes: 12,
        digest: 'digest2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    compressedSizeBytes: 154,
    digest: 'digest0',
    registryName: 'registry_name4',
    repository: 'repository4',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  manifestCount: 1,
  name: 'repo-1',
  registryName: 'example',
  tagCount: 1,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



