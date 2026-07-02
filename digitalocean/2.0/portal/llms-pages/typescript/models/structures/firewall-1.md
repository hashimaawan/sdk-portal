# Firewall 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkZpcmV3YWxsMQ

An object specifying allow and deny rules to control traffic to the load balancer.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Firewall1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allow` | `string[] \| undefined` | Optional | the rules for allowing traffic to the load balancer (in the form 'ip:1.2.3.4' or 'cidr:1.2.0.0/16') |
| `deny` | `string[] \| undefined` | Optional | the rules for denying traffic to the load balancer (in the form 'ip:1.2.3.4' or 'cidr:1.2.0.0/16') |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Firewall1 } from 'digitalocean-apilib';

const firewall1: Firewall1 = {
  allow: [
    'ip:1.2.3.4',
    'cidr:2.3.0.0/16'
  ],
  deny: [
    'ip:1.2.3.4',
    'cidr:2.3.0.0/16'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



