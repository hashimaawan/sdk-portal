# Mysql

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRk15c3Fs

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Mysql`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `regions` | `string[] \| undefined` | Optional, Read-only | An array of strings containing the names of available regions |
| `versions` | `string[] \| undefined` | Optional, Read-only | An array of strings containing the names of available regions |
| `layouts` | [`Layout[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/layout.md) | Optional, Read-only | An array of objects, each indicating the node sizes (otherwise referred to as slugs) that are available with various numbers of nodes in the database cluster. Each slugs denotes the node's identifier, CPU, and RAM (in that order). |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Mysql } from 'digitalocean-apilib';

const mysql: Mysql = {
  regions: [
    'ams3',
    'blr1'
  ],
  versions: [
    '4.4',
    '5.0'
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
};
```



