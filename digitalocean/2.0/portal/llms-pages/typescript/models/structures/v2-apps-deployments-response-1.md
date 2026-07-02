# V2 Apps Deployments Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBEZXBsb3ltZW50cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2AppsDeploymentsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deployment` | [`AnAppDeployment \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/an-app-deployment.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2AppsDeploymentsResponse1 } from 'digitalocean-apilib';

const v2AppsDeploymentsResponse1: V2AppsDeploymentsResponse1 = {
  deployment: {
    cause: 'cause8',
    clonedFrom: 'cloned_from0',
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
    id: 'id2',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



