# Floating Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA

An objects containing information about a resource associated with a Droplet.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`FloatingIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cost` | `string \| undefined` | Optional | The cost of the resource in USD per month if the resource is retained after the Droplet is destroyed. |
| `id` | `string \| undefined` | Optional | The unique identifier for the resource associated with the Droplet. |
| `name` | `string \| undefined` | Optional | The name of the resource associated with the Droplet. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { FloatingIp } from 'digitalocean-apilib';

const floatingIp: FloatingIp = {
  cost: '0.05',
  id: '61486916',
  name: 'ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



