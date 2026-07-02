# Resources 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc291cmNlczI

An embedded object containing key value pairs of resource type and resource statistics. It also includes a count of the total number of resources tagged with the current tag as well as a `last_tagged_uri` attribute set to the last resource tagged with the current tag.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Resources2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `count` | `number \| undefined` | Optional | The number of tagged objects for this type of resource.<br><br>**Constraints**: `>= 0` |
| `lastTaggedUri` | `string \| undefined` | Optional | The URI for the last tagged object for this type of resource. |
| `databases` | [`Databases \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `droplets` | [`Databases \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `imgages` | [`Databases \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `volumeSnapshots` | [`Databases \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `volumes` | [`Databases \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Resources2 } from 'digitalocean-apilib';

const resources2: Resources2 = {
  count: 5,
  lastTaggedUri: 'https://api.digitalocean.com/v2/images/7555620',
  databases: {
    count: 1,
    lastTaggedUri: 'https://api.digitalocean.com/v2/databases/b92438f6-ba03-416c-b642-e9236db91976',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  droplets: {
    count: 1,
    lastTaggedUri: 'https://api.digitalocean.com/v2/droplets/3164444',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  imgages: {
    count: 158,
    lastTaggedUri: 'last_tagged_uri4',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  volumeSnapshots: {
    count: 1,
    lastTaggedUri: 'https://api.digitalocean.com/v2/snapshots/1f6f46e8-6b60-11e9-be4e-0a58ac144519',
  },
  volumes: {
    count: 1,
    lastTaggedUri: 'https://api.digitalocean.com/v2/volumes/3d80cb72-342b-4aaa-b92e-4e4abb24a933',
  },
  additionalProperties: {
    'images': { 'count': 1, 'last_tagged_uri': 'https: //api.digitalocean.com/v2/images/7555620' }
  },
};
```



