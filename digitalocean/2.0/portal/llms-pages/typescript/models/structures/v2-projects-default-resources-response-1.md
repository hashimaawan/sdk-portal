# V2 Projects Default Resources Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2ProjectsDefaultResourcesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resources` | [`Resources1[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/resources-1.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Status14,
  V2ProjectsDefaultResourcesResponse1,
} from 'digitalocean-apilib';

const v2ProjectsDefaultResourcesResponse1: V2ProjectsDefaultResourcesResponse1 = {
  resources: [
    {
      assignedAt: '2018-09-28T19:26:37Z',
      links: {
        self: 'https://api.digitalocean.com/v2/droplets/13457723',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      status: Status14.Ok,
      urn: 'do:droplet:13457723',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      assignedAt: '2019-03-31T16:24:14Z',
      links: {
        self: 'https://api.digitalocean.com/v2/domains/example.com',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      status: Status14.Ok,
      urn: 'do:domain:example.com',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



