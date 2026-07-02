# Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc291cmNlcw

An object containing additional information about resource related to a Droplet requested to be destroyed.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Resources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `floatingIps` | [`Droplet1[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/droplet-1.md) | Optional | - |
| `reservedIps` | [`Droplet1[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/droplet-1.md) | Optional | - |
| `snapshots` | [`Droplet1[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/droplet-1.md) | Optional | - |
| `volumeSnapshots` | [`Droplet1[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/droplet-1.md) | Optional | - |
| `volumes` | [`Droplet1[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/droplet-1.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Resources } from 'digitalocean-apilib';

const resources: Resources = {
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
};
```



