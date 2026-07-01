# Load Balancers Actions Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQXR0YWNoJTI1MjBUbyUyNTIwTmV0d29yayUyNTIwUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`LoadBalancersActionsAttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip` | `string \| undefined` | Optional | IP to request to be assigned to this Load Balancer; if you do not provide this then you will be auto assigned an IP address |
| `network` | `number` | Required | ID of an existing network to attach the Load Balancer to |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  LoadBalancersActionsAttachToNetworkRequest,
} from 'hetzner-cloud-apilib';

const loadBalancersActionsAttachToNetworkRequest: LoadBalancersActionsAttachToNetworkRequest = {
  network: 4711,
  ip: '10.0.1.1',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



