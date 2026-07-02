# Repository

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlcG9zaXRvcnk

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Repository`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `latestTag` | [`LatestTag \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/latest-tag.md) | Optional | - |
| `name` | `string \| undefined` | Optional | The name of the repository. |
| `registryName` | `string \| undefined` | Optional | The name of the container registry. |
| `tagCount` | `number \| undefined` | Optional | The number of tags in the repository. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Repository } from 'digitalocean-apilib';

const repository: Repository = {
  latestTag: {
    compressedSizeBytes: 108,
    manifestDigest: 'manifest_digest2',
    registryName: 'registry_name4',
    repository: 'repository4',
    sizeBytes: 226,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  name: 'repo-1',
  registryName: 'example',
  tagCount: 1,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



