# V2 Apps Deployments Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBEZXBsb3ltZW50cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2AppsDeploymentsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deployments` | [`AnAppDeployment[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/an-app-deployment.md) | Optional | - |
| `links` | [`Links \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/meta.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2AppsDeploymentsResponse } from 'digitalocean-apilib';

const v2AppsDeploymentsResponse: V2AppsDeploymentsResponse = {
  meta: {
    total: 1,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  deployments: [
    {
      cause: 'cause2',
      clonedFrom: 'cloned_from4',
      createdAt: '2016-03-13T12:52:32.123Z',
      functions: [
        {
          name: 'name4',
          namespace: 'namespace8',
          sourceCommitHash: 'source_commit_hash4',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      id: 'id6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      cause: 'cause2',
      clonedFrom: 'cloned_from4',
      createdAt: '2016-03-13T12:52:32.123Z',
      functions: [
        {
          name: 'name4',
          namespace: 'namespace8',
          sourceCommitHash: 'source_commit_hash4',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      id: 'id6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      cause: 'cause2',
      clonedFrom: 'cloned_from4',
      createdAt: '2016-03-13T12:52:32.123Z',
      functions: [
        {
          name: 'name4',
          namespace: 'namespace8',
          sourceCommitHash: 'source_commit_hash4',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      id: 'id6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  links: {
    pages: {
      last: 'last6',
      next: 'next2',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
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



