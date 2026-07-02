# Sources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlNvdXJjZXM

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Sources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `addresses` | `string[] \| undefined` | Optional | An array of strings containing the IPv4 addresses, IPv6 addresses, IPv4 CIDRs, and/or IPv6 CIDRs to which the firewall will allow traffic. |
| `dropletIds` | `number[] \| undefined` | Optional | An array containing the IDs of the Droplets to which the firewall will allow traffic. |
| `kubernetesIds` | `string[] \| undefined` | Optional | An array containing the IDs of the Kubernetes clusters to which the firewall will allow traffic. |
| `loadBalancerUids` | `string[] \| undefined` | Optional | An array containing the IDs of the load balancers to which the firewall will allow traffic. |
| `tags` | `string[] \| null \| undefined` | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Sources } from 'digitalocean-apilib';

const sources: Sources = {
  addresses: [
    '1.2.3.4',
    '18.0.0.0/8'
  ],
  dropletIds: [
    8043964
  ],
  kubernetesIds: [
    '41b74c5d-9bd0-5555-5555-a57c495b81a3'
  ],
  loadBalancerUids: [
    '4de7ac8b-495b-4884-9a69-1050c6793cd6'
  ],
  tags: [
    'tags1',
    'tags2',
    'tags3'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



