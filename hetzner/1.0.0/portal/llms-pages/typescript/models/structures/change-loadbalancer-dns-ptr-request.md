# Change Loadbalancer Dns Ptr Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNoYW5nZUxvYWRiYWxhbmNlckRuc1B0clJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`ChangeLoadbalancerDnsPtrRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dnsPtr` | `string \| null` | Required | Hostname to set as a reverse DNS PTR entry |
| `ip` | `string` | Required | Public IP address for which the reverse DNS entry should be set |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ChangeLoadbalancerDnsPtrRequest } from 'hetzner-cloud-apilib';

const changeLoadbalancerDnsPtrRequest: ChangeLoadbalancerDnsPtrRequest = {
  dnsPtr: 'lb1.example.com',
  ip: '1.2.3.4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



