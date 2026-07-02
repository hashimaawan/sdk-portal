# Layout

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkxheW91dA

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Layout`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `numNodes` | `number \| undefined` | Optional | - |
| `sizes` | `string[] \| undefined` | Optional, Read-only | An array of objects containing the slugs available with various node counts |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Layout } from 'digitalocean-apilib';

const layout: Layout = {
  numNodes: 1,
  sizes: [
    'db-s-1vcpu-1gb',
    'db-s-1vcpu-2gb'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



