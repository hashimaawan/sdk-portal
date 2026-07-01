# Load Balancers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVxdWVzdA


# Interface Name

`LoadBalancersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string \| undefined` | Optional | New Load Balancer name |


# Example

```ts
import { LoadBalancersRequest } from 'hetzner-cloud-apilib';

const loadBalancersRequest: LoadBalancersRequest = {
  labels: { 'labelkey': 'value' },
  name: 'new-name',
};
```



