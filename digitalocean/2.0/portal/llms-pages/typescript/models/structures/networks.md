# Networks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRk5ldHdvcmtz

The details of the network that are configured for the Droplet instance.  This is an object that contains keys for IPv4 and IPv6.  The value of each of these is an array that contains objects describing an individual IP resource allocated to the Droplet.  These will define attributes like the IP address, netmask, and gateway of the specific network depending on the type of network it is.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Networks`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `v4` | [`V4[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v4.md) | Optional | - |
| `v6` | [`V6[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v6.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Networks, Type10, Type11 } from 'digitalocean-apilib';

const networks: Networks = {
  v4: [
    {
      gateway: 'gateway2',
      ipAddress: 'ip_address2',
      netmask: 'netmask2',
      type: Type10.Public,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      gateway: 'gateway2',
      ipAddress: 'ip_address2',
      netmask: 'netmask2',
      type: Type10.Public,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      gateway: 'gateway2',
      ipAddress: 'ip_address2',
      netmask: 'netmask2',
      type: Type10.Public,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  v6: [
    {
      gateway: 'gateway4',
      ipAddress: 'ip_address4',
      netmask: 106,
      type: Type11.Public,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      gateway: 'gateway4',
      ipAddress: 'ip_address4',
      netmask: 106,
      type: Type11.Public,
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



