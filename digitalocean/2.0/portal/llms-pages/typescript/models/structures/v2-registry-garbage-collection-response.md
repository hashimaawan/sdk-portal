# V2 Registry Garbage Collection Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwR2FyYmFnZSUyNTIwQ29sbGVjdGlvbiUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2RegistryGarbageCollectionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `garbageCollection` | [`GarbageCollection \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/garbage-collection.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Status15,
  V2RegistryGarbageCollectionResponse,
} from 'digitalocean-apilib';

const v2RegistryGarbageCollectionResponse: V2RegistryGarbageCollectionResponse = {
  garbageCollection: {
    blobsDeleted: 40,
    createdAt: '2016-03-13T12:52:32.123Z',
    freedBytes: 86,
    registryName: 'registry_name6',
    status: Status15.Succeeded,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



