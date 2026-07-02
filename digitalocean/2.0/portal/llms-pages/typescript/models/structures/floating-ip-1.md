# Floating Ip 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkZsb2F0aW5nSXAx

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`FloatingIp1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet` | [`FloatingIp1Droplet \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/oneof-anyof-definitions/floating-ip-1-droplet.md) | Optional | This is a container for any-of cases. |
| `ip` | `string \| undefined` | Optional | The public IP address of the floating IP. It also serves as its identifier. |
| `locked` | `boolean \| undefined` | Optional | A boolean value indicating whether or not the floating IP has pending actions preventing new ones from being submitted. |
| `projectId` | `string \| undefined` | Optional | The UUID of the project to which the reserved IP currently belongs. |
| `region` | [`Region \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/region.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { FloatingIp1 } from 'digitalocean-apilib';

const floatingIp1: FloatingIp1 = {
  droplet: { 'key1': 'val1', 'key2': 'val2' },
  ip: '45.55.96.47',
  locked: true,
  projectId: '746c6152-2fa2-11ed-92d3-27aaa54e4988',
  region: {
    available: false,
    features: [
      'features7',
      'features8',
      'features9'
    ],
    name: 'name6',
    sizes: [
      'sizes6'
    ],
    slug: 'slug0',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



