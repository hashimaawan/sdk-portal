# Load Balancer Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2U


# Interface Name

`LoadBalancerService`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `destinationPort` | `number` | Required | Port the Load Balancer will balance to |
| `healthCheck` | [`LoadBalancerServiceHealthCheck`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/load-balancer-service-health-check.md) | Required | Service health check |
| `http` | [`LoadBalancerServiceHTTP \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/load-balancer-service-http.md) | Optional | Configuration option for protocols http and https |
| `listenPort` | `number` | Required | Port the Load Balancer listens on |
| `protocol` | [`Protocol7Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/protocol-7.md) | Required | Protocol of the Load Balancer |
| `proxyprotocol` | `boolean` | Required | Is Proxyprotocol enabled or not |


# Example

```ts
import {
  LoadBalancerService,
  Protocol6Enum,
  Protocol7Enum,
} from 'hetzner-cloud-apilib';

const loadBalancerService: LoadBalancerService = {
  destinationPort: 80,
  healthCheck: {
    interval: 15,
    port: 4711,
    protocol: Protocol6Enum.Http,
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
  },
  listenPort: 443,
  protocol: Protocol7Enum.Https,
  proxyprotocol: false,
  http: {
    certificates: [
      180
    ],
    cookieLifetime: 160,
    cookieName: 'cookie_name6',
    redirectHttp: false,
    stickySessions: false,
  },
};
```



