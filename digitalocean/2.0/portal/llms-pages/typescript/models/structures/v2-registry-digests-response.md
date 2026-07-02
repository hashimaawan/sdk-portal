# V2 Registry Digests Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwRGlnZXN0cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2RegistryDigestsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `manifests` | [`LatestManifest[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/latest-manifest.md) | Optional | - |
| `links` | [`Links \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/meta.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2RegistryDigestsResponse } from 'digitalocean-apilib';

const v2RegistryDigestsResponse: V2RegistryDigestsResponse = {
  meta: {
    total: 3,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  manifests: [
    {
      blobs: [
        {
          compressedSizeBytes: 1471,
          digest: 'sha256:14119a10abf4669e8cdbdff324a9f9605d99697215a0d21c360fe8dfa8471bab',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          compressedSizeBytes: 12,
          digest: 'sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e',
          additionalProperties: {
            'compressed_size_byte': 2814446
          },
        },
        {
          compressedSizeBytes: 528,
          digest: 'sha256:69704ef328d05a9f806b6b8502915e6a0a4faa4d72018dc42343f511490daf8a',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      compressedSizeBytes: 1972332,
      digest: 'sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221',
      registryName: 'example',
      repository: 'repo-1',
      sizeBytes: 2816445,
      tags: [
        'v1',
        'v2'
      ],
      updatedAt: '2021-04-09T23:54:25Z',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  links: {
    pages: {
      last: 'https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=3&per_page=1',
      next: 'https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=3&per_page=1',
      additionalProperties: {
        'first': 'https: //api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=1&per_page=1',
        'prev': 'https: //api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=1&per_page=1'
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



