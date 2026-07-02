# Latest Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkxhdGVzdFRhZw

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`LatestTag`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `compressedSizeBytes` | `number \| undefined` | Optional | The compressed size of the tag in bytes. |
| `manifestDigest` | `string \| undefined` | Optional | The digest of the manifest associated with the tag. |
| `registryName` | `string \| undefined` | Optional | The name of the container registry. |
| `repository` | `string \| undefined` | Optional | The name of the repository. |
| `sizeBytes` | `number \| undefined` | Optional | The uncompressed size of the tag in bytes (this size is calculated asynchronously so it may not be immediately available). |
| `tag` | `string \| undefined` | Optional | The name of the tag. |
| `updatedAt` | `string \| undefined` | Optional | The time the tag was last updated. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { LatestTag } from 'digitalocean-apilib';

const latestTag: LatestTag = {
  compressedSizeBytes: 2803255,
  manifestDigest: 'sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221',
  registryName: 'example',
  repository: 'repo-1',
  sizeBytes: 5861888,
  tag: 'latest',
  updatedAt: '2020-04-09T23:54:25Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



