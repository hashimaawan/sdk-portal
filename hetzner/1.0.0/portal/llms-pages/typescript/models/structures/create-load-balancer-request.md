# Create Load Balancer Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZUxvYWRCYWxhbmNlclJlcXVlc3Q


# Interface Name

`CreateLoadBalancerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `algorithm` | [`LoadBalancerAlgorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/load-balancer-algorithm.md) | Required | Algorithm of the Load Balancer |
| `labels` | [`Labels \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `loadBalancerType` | `string` | Required | ID or name of the Load Balancer type this Load Balancer should be created with |
| `location` | `string \| undefined` | Optional | ID or name of Location to create Load Balancer in |
| `name` | `string` | Required | Name of the Load Balancer |
| `network` | `number \| undefined` | Optional | ID of the network the Load Balancer should be attached to on creation |
| `networkZone` | `string \| undefined` | Optional | Name of network zone |
| `publicInterface` | `boolean \| undefined` | Optional | Enable or disable the public interface of the Load Balancer |
| `services` | [`LoadBalancerService[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/load-balancer-service.md) | Optional | Array of services |
| `targets` | [`LoadBalancerTarget[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/load-balancer-target.md) | Optional | Array of targets |


# Example

```ts
import { CreateLoadBalancerRequest, Type28Enum } from 'hetzner-cloud-apilib';

const createLoadBalancerRequest: CreateLoadBalancerRequest = {
  algorithm: {
    type: Type28Enum.RoundRobin,
  },
  loadBalancerType: 'lb11',
  name: 'Web Frontend',
  labels: {
    labelkey: 'labelkey4',
  },
  location: 'location2',
  network: 123,
  networkZone: 'eu-central',
  publicInterface: true,
};
```



