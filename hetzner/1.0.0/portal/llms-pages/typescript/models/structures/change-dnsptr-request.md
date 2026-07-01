# Change DNSPTR Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNoYW5nZUROU1BUUlJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`ChangeDnsptrRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dnsPtr` | `string \| null` | Required | Hostname to set as a reverse DNS PTR entry, will reset to original default value if `null` |
| `ip` | `string` | Required | IP address for which to set the reverse DNS entry |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ChangeDnsptrRequest } from 'hetzner-cloud-apilib';

const changeDnsptrRequest: ChangeDnsptrRequest = {
  dnsPtr: 'server02.example.com',
  ip: '1.2.3.4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



