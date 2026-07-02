# Latest Manifest

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkxhdGVzdE1hbmlmZXN0

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`LatestManifest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blobs` | [`Blob[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/blob.md) | Optional | All blobs associated with this manifest |
| `compressedSizeBytes` | `number \| undefined` | Optional | The compressed size of the manifest in bytes. |
| `digest` | `string \| undefined` | Optional | The manifest digest |
| `registryName` | `string \| undefined` | Optional | The name of the container registry. |
| `repository` | `string \| undefined` | Optional | The name of the repository. |
| `sizeBytes` | `number \| undefined` | Optional | The uncompressed size of the manifest in bytes (this size is calculated asynchronously so it may not be immediately available). |
| `tags` | `string[] \| undefined` | Optional | All tags associated with this manifest |
| `updatedAt` | `string \| undefined` | Optional | The time the manifest was last updated. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { LatestManifest } from 'digitalocean-apilib';

const latestManifest: LatestManifest = {
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
    }
  ],
  compressedSizeBytes: 2803255,
  digest: 'sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221',
  registryName: 'example',
  repository: 'repo-1',
  sizeBytes: 5861888,
  tags: [
    'latest',
    'v1',
    'v2'
  ],
  updatedAt: '2020-04-09T23:54:25Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



