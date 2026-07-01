# Load Balancer Service Health Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2VIZWFsdGhDaGVjaw

Service health check


# Interface Name

`LoadBalancerServiceHealthCheck`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `http` | [`Http \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/http.md) | Optional | Additional configuration for protocol http |
| `interval` | `number` | Required | Time interval in seconds health checks are performed |
| `port` | `number` | Required | Port the health check will be performed on |
| `protocol` | [`Protocol6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/protocol-6.md) | Required | Type of the health check |
| `retries` | `number` | Required | Unsuccessful retries needed until a target is considered unhealthy; an unhealthy target needs the same number of successful retries to become healthy again |
| `timeout` | `number` | Required | Time in seconds after an attempt is considered a timeout |


# Example

```ts
import {
  LoadBalancerServiceHealthCheck,
  Protocol6,
} from 'hetzner-cloud-apilib';

const loadBalancerServiceHealthCheck: LoadBalancerServiceHealthCheck = {
  interval: 15,
  port: 4711,
  protocol: Protocol6.Http,
  retries: 3,
  timeout: 10,
  http: {
    domain: 'domain4',
    path: 'path2',
    response: 'response8',
    statusCodes: [
      'status_codes0',
      'status_codes1',
      'status_codes2'
    ],
    tls: false,
  },
};
```



