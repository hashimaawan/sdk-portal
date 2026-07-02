# V2 Databases Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9wdGlvbnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DatabasesOptionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `options` | [`Options \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/options.md) | Optional | - |
| `versionAvailability` | [`VersionAvailability \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/version-availability.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2DatabasesOptionsResponse } from 'digitalocean-apilib';

const v2DatabasesOptionsResponse: V2DatabasesOptionsResponse = {
  options: {
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
  },
  versionAvailability: {
    mongodb: [
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
    mysql: [
      {
        endOfAvailability: 'end_of_availability0',
        endOfLife: 'end_of_life0',
        version: 'version0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
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



