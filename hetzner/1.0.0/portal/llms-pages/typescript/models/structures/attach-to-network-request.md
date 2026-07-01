# Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkF0dGFjaFRvTmV0d29ya1JlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`AttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `aliasIps` | `string[] \| undefined` | Optional | Additional IPs to be assigned to this Server |
| `ip` | `string \| undefined` | Optional | IP to request to be assigned to this Server; if you do not provide this then you will be auto assigned an IP address |
| `network` | `number` | Required | ID of an existing network to attach the Server to |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { AttachToNetworkRequest } from 'hetzner-cloud-apilib';

const attachToNetworkRequest: AttachToNetworkRequest = {
  network: 4711,
  aliasIps: [
    '10.0.1.2'
  ],
  ip: '10.0.1.1',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



