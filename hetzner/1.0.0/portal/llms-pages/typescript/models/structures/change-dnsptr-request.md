# Change DNSPTR Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNoYW5nZUROU1BUUlJlcXVlc3Q


# Interface Name

`ChangeDNSPTRRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dnsPtr` | `string \| null` | Required | Hostname to set as a reverse DNS PTR entry, will reset to original default value if `null` |
| `ip` | `string` | Required | IP address for which to set the reverse DNS entry |


# Example

```ts
import { ChangeDNSPTRRequest } from 'hetzner-cloud-apilib';

const changeDNSPTRRequest: ChangeDNSPTRRequest = {
  dnsPtr: 'server02.example.com',
  ip: '1.2.3.4',
};
```



