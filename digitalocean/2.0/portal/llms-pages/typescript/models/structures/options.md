# Options

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRk9wdGlvbnM

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Options`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mongodb` | [`Mongodb \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/mongodb.md) | Optional | - |
| `mysql` | [`Mysql \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/mysql.md) | Optional | - |
| `pg` | [`Pg \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/pg.md) | Optional | - |
| `redis` | [`Redis \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/redis.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Options } from 'digitalocean-apilib';

const options: Options = {
  mongodb: {
    regions: [
      'regions3',
      'regions4'
    ],
    versions: [
      'versions3',
      'versions4'
    ],
    layouts: [
      {
        numNodes: 190,
        sizes: [
          'sizes2',
          'sizes3'
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        numNodes: 190,
        sizes: [
          'sizes2',
          'sizes3'
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  mysql: {
    regions: [
      'regions9',
      'regions0',
      'regions1'
    ],
    versions: [
      'versions9',
      'versions0',
      'versions1'
    ],
    layouts: [
      {
        numNodes: 190,
        sizes: [
          'sizes2',
          'sizes3'
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        numNodes: 190,
        sizes: [
          'sizes2',
          'sizes3'
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        numNodes: 190,
        sizes: [
          'sizes2',
          'sizes3'
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  pg: {
    regions: [
      'regions3'
    ],
    versions: [
      'versions3'
    ],
    layouts: [
      {
        numNodes: 190,
        sizes: [
          'sizes2',
          'sizes3'
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  redis: {
    regions: [
      'regions7'
    ],
    versions: [
      'versions7'
    ],
    layouts: [
      {
        numNodes: 190,
        sizes: [
          'sizes2',
          'sizes3'
        ],
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



