# V2 Load Balancers Droplets Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMERyb3BsZXRzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2LoadBalancersDropletsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dropletIds` | `number[] \| undefined` | Optional | An array containing the IDs of the Droplets assigned to the load balancer. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2LoadBalancersDropletsRequest } from 'digitalocean-apilib';

const v2LoadBalancersDropletsRequest: V2LoadBalancersDropletsRequest = {
  dropletIds: [
    3164444,
    3164445
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



