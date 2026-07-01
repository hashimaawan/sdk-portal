# Load Balancer Service HTTP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2VIVFRQ

Configuration option for protocols http and https

*This model accepts additional fields of type unknown.*


# Interface Name

`LoadBalancerServiceHttp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificates` | `number[] \| undefined` | Optional | IDs of the Certificates to use for TLS/SSL termination by the Load Balancer; empty for TLS/SSL passthrough or if `protocol` is "http" |
| `cookieLifetime` | `number \| undefined` | Optional | Lifetime of the cookie used for sticky sessions |
| `cookieName` | `string \| undefined` | Optional | Name of the cookie used for sticky sessions |
| `redirectHttp` | `boolean \| undefined` | Optional | Redirect HTTP requests to HTTPS. Only available if protocol is "https". Default `false` |
| `stickySessions` | `boolean \| undefined` | Optional | Use sticky sessions. Only available if protocol is "http" or "https". Default `false` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { LoadBalancerServiceHttp } from 'hetzner-cloud-apilib';

const loadBalancerServiceHttp: LoadBalancerServiceHttp = {
  certificates: [
    897
  ],
  cookieLifetime: 300,
  cookieName: 'HCLBSTICKY',
  redirectHttp: true,
  stickySessions: true,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



