# Load Balancers Actions Delete Service Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGVsZXRlJTI1MjBTZXJ2aWNlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`LoadBalancersActionsDeleteServiceRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `listenPort` | `number` | Required | The listen port of the service you want to delete |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  LoadBalancersActionsDeleteServiceRequest,
} from 'hetzner-cloud-apilib';

const loadBalancersActionsDeleteServiceRequest: LoadBalancersActionsDeleteServiceRequest = {
  listenPort: 4711,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



