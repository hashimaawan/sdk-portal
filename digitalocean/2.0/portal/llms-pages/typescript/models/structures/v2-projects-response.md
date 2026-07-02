# V2 Projects Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2ProjectsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projects` | [`Project[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/project.md) | Optional | - |
| `links` | [`Links \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/meta.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { MEnvironment, V2ProjectsResponse } from 'digitalocean-apilib';

const v2ProjectsResponse: V2ProjectsResponse = {
  meta: {
    total: 2,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  projects: [
    {
      createdAt: '2018-09-27T20:10:35Z',
      description: 'My website API',
      environment: MEnvironment.Production,
      id: '4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679',
      name: 'my-web-api',
      ownerId: 258992,
      ownerUuid: '99525febec065ca37b2ffe4f852fd2b2581895e7',
      purpose: 'Service or API',
      updatedAt: '2018-09-27T20:10:35Z',
      isDefault: false,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
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
    }
  ],
  links: {
    pages: {
      last: 'https://api.digitalocean.com/v2/projects?page=1',
      next: 'next2',
      additionalProperties: {
        'first': 'https: //api.digitalocean.com/v2/projects?page=1'
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



