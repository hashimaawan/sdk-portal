# Load Balancers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`LoadBalancersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mDelete` | `boolean \| undefined` | Optional | If true, prevents the Load Balancer from being deleted |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  LoadBalancersActionsChangeProtectionRequest,
} from 'hetzner-cloud-apilib';

const loadBalancersActionsChangeProtectionRequest: LoadBalancersActionsChangeProtectionRequest = {
  mDelete: true,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



