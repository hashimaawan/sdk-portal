# V2 Projects Default Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2ProjectsDefaultResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `project` | [`Project \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/project.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { MEnvironment, V2ProjectsDefaultResponse } from 'digitalocean-apilib';

const v2ProjectsDefaultResponse: V2ProjectsDefaultResponse = {
  project: {
    createdAt: '2017-10-19T21:44:20Z',
    description: 'Default project',
    environment: MEnvironment.Development,
    id: 'addb4547-6bab-419a-8542-76263a033cf6',
    name: 'Default',
    ownerId: 258992,
    ownerUuid: '99525febec065ca37b2ffe4f852fd2b2581895e7',
    purpose: 'Just trying out DigitalOcean',
    updatedAt: '2019-11-05T18:50:03Z',
    isDefault: true,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



