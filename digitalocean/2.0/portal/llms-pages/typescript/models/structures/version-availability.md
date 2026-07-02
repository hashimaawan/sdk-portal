# Version Availability

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlZlcnNpb25BdmFpbGFiaWxpdHk

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`VersionAvailability`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mongodb` | [`Mongodb1[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `mysql` | [`Mongodb1[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `pg` | [`Mongodb1[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `redis` | [`Mongodb1[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { VersionAvailability } from 'digitalocean-apilib';

const versionAvailability: VersionAvailability = {
  mongodb: [
    {
      endOfAvailability: 'end_of_availability4',
      endOfLife: 'end_of_life4',
      version: 'version4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  mysql: [
    {
      endOfAvailability: 'end_of_availability0',
      endOfLife: 'end_of_life0',
      version: 'version0',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  pg: [
    {
      endOfAvailability: 'end_of_availability4',
      endOfLife: 'end_of_life4',
      version: 'version4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      endOfAvailability: 'end_of_availability4',
      endOfLife: 'end_of_life4',
      version: 'version4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      endOfAvailability: 'end_of_availability4',
      endOfLife: 'end_of_life4',
      version: 'version4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  redis: [
    {
      endOfAvailability: 'end_of_availability8',
      endOfLife: 'end_of_life8',
      version: 'version8',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      endOfAvailability: 'end_of_availability8',
      endOfLife: 'end_of_life8',
      version: 'version8',
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



