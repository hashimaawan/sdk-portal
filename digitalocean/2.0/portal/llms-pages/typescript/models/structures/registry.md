# Registry

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlZ2lzdHJ5

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Registry`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the registry was created. |
| `name` | `string \| undefined` | Optional | A globally unique name for the container registry. Must be lowercase and be composed only of numbers, letters and `-`, up to a limit of 63 characters.<br><br>**Constraints**: *Maximum Length*: `63`, *Pattern*: `^[a-z0-9-]{1,63}$` |
| `region` | `string \| undefined` | Optional | Slug of the region where registry data is stored |
| `storageUsageBytes` | `number \| undefined` | Optional, Read-only | The amount of storage used in the registry in bytes. |
| `storageUsageBytesUpdatedAt` | `string \| undefined` | Optional, Read-only | The time at which the storage usage was updated. Storage usage is calculated asynchronously, and may not immediately reflect pushes to the registry. |
| `subscription` | [`Subscription \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/subscription.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Registry } from 'digitalocean-apilib';

const registry: Registry = {
  createdAt: '2020-03-21T16:02:37Z',
  name: 'example',
  region: 'fra1',
  storageUsageBytes: 29393920,
  storageUsageBytesUpdatedAt: '2020-11-04T21:39:49.530562231Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



