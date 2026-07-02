# V2 Droplets Destroy with Associated Resources Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTdGF0dXMlMjUyMFJlc3BvbnNl

An objects containing information about a resources scheduled for deletion.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DropletsDestroyWithAssociatedResourcesStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `completedAt` | `string \| undefined` | Optional | A time value given in ISO8601 combined date and time format indicating when the requested action was completed. |
| `droplet` | [`Droplet1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/droplet-1.md) | Optional | An object containing information about a resource scheduled for deletion. |
| `failures` | `number \| undefined` | Optional | A count of the associated resources that failed to be destroyed, if any. |
| `resources` | [`Resources \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/resources.md) | Optional | An object containing additional information about resource related to a Droplet requested to be destroyed. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  V2DropletsDestroyWithAssociatedResourcesStatusResponse,
} from 'digitalocean-apilib';

const v2DropletsDestroyWithAssociatedResourcesStatusResponse: V2DropletsDestroyWithAssociatedResourcesStatusResponse = {
  completedAt: '2020-04-01T18:11:49Z',
  droplet: {
    destroyedAt: '2016-03-13T12:52:32.123Z',
    errorMessage: 'error_message2',
    id: 'id0',
    name: 'name0',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  failures: 0,
  resources: {
    floatingIps: [
      {
        destroyedAt: '2016-03-13T12:52:32.123Z',
        errorMessage: 'error_message4',
        id: 'id2',
        name: 'name2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        destroyedAt: '2016-03-13T12:52:32.123Z',
        errorMessage: 'error_message4',
        id: 'id2',
        name: 'name2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        destroyedAt: '2016-03-13T12:52:32.123Z',
        errorMessage: 'error_message4',
        id: 'id2',
        name: 'name2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    reservedIps: [
      {
        destroyedAt: '2016-03-13T12:52:32.123Z',
        errorMessage: 'error_message2',
        id: 'id0',
        name: 'name0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        destroyedAt: '2016-03-13T12:52:32.123Z',
        errorMessage: 'error_message2',
        id: 'id0',
        name: 'name0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    snapshots: [
      {
        destroyedAt: '2016-03-13T12:52:32.123Z',
        errorMessage: 'error_message4',
        id: 'id2',
        name: 'name2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        destroyedAt: '2016-03-13T12:52:32.123Z',
        errorMessage: 'error_message4',
        id: 'id2',
        name: 'name2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        destroyedAt: '2016-03-13T12:52:32.123Z',
        errorMessage: 'error_message4',
        id: 'id2',
        name: 'name2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    volumeSnapshots: [
      {
        destroyedAt: '2016-03-13T12:52:32.123Z',
        errorMessage: 'error_message0',
        id: 'id8',
        name: 'name8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        destroyedAt: '2016-03-13T12:52:32.123Z',
        errorMessage: 'error_message0',
        id: 'id8',
        name: 'name8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    volumes: [
      {
        destroyedAt: '2016-03-13T12:52:32.123Z',
        errorMessage: 'error_message8',
        id: 'id6',
        name: 'name6',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



