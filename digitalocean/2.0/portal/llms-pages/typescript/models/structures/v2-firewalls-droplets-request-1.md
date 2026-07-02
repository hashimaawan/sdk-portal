# V2 Firewalls Droplets Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMERyb3BsZXRzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2FirewallsDropletsRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dropletIds` | `number[]` | Required | An array containing the IDs of the Droplets to be assigned to the firewall. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2FirewallsDropletsRequest1 } from 'digitalocean-apilib';

const v2FirewallsDropletsRequest1: V2FirewallsDropletsRequest1 = {
  dropletIds: [
    49696269
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



