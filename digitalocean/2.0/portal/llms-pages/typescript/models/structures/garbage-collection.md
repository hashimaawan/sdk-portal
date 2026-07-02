# Garbage Collection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkdhcmJhZ2VDb2xsZWN0aW9u

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`GarbageCollection`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blobsDeleted` | `number \| undefined` | Optional | The number of blobs deleted as a result of this garbage collection. |
| `createdAt` | `string \| undefined` | Optional | The time the garbage collection was created. |
| `freedBytes` | `number \| undefined` | Optional | The number of bytes freed as a result of this garbage collection. |
| `registryName` | `string \| undefined` | Optional | The name of the container registry. |
| `status` | [`Status15 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status-15.md) | Optional | The current status of this garbage collection. |
| `updatedAt` | `string \| undefined` | Optional | The time the garbage collection was last updated. |
| `uuid` | `string \| undefined` | Optional | A string specifying the UUID of the garbage collection. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { GarbageCollection, Status15 } from 'digitalocean-apilib';

const garbageCollection: GarbageCollection = {
  blobsDeleted: 42,
  createdAt: '2020-10-30T21:03:24Z',
  freedBytes: 667,
  registryName: 'example',
  status: Status15.Requested,
  updatedAt: '2020-10-30T21:03:44Z',
  uuid: 'eff0feee-49c7-4e8f-ba5c-a320c109c8a8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



