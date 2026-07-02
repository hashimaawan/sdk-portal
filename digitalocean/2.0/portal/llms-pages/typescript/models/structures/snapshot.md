# Snapshot

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlNuYXBzaG90

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Snapshot`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Required | The unique identifier for the snapshot. |
| `createdAt` | `string` | Required | A time value given in ISO8601 combined date and time format that represents when the snapshot was created. |
| `minDiskSize` | `number` | Required | The minimum size in GB required for a volume or Droplet to use this snapshot. |
| `name` | `string` | Required | A human-readable name for the snapshot. |
| `regions` | `string[]` | Required | An array of the regions that the snapshot is available in. The regions are represented by their identifying slug values. |
| `sizeGigabytes` | `number` | Required | The billable size of the snapshot in gigabytes. |
| `resourceId` | `string` | Required | The unique identifier for the resource that the snapshot originated from. |
| `resourceType` | [`ResourceType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/resource-type-1.md) | Required | The type of resource that the snapshot originated from. |
| `tags` | `string[] \| null` | Required | An array of Tags the snapshot has been tagged with. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { ResourceType1, Snapshot } from 'digitalocean-apilib';

const snapshot: Snapshot = {
  id: '6372321',
  createdAt: '2020-07-28T16:47:44Z',
  minDiskSize: 25,
  name: 'web-01-1595954862243',
  regions: [
    'nyc3',
    'sfo3'
  ],
  sizeGigabytes: 2.34,
  resourceId: '200776916',
  resourceType: ResourceType1.Droplet,
  tags: [
    'web',
    'env:prod'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



