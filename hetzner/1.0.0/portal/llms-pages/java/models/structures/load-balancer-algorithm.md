# Load Balancer Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlckFsZ29yaXRobQ

Algorithm of the Load Balancer


# Class Name

`LoadBalancerAlgorithm`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type28Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-28.md) | Required | Type of the algorithm | Type28Enum getType() | setType(Type28Enum type) |


# Example

```java
import cloud.hetzner.api.models.LoadBalancerAlgorithm;
import cloud.hetzner.api.models.Type28Enum;

LoadBalancerAlgorithm loadBalancerAlgorithm = new LoadBalancerAlgorithm.Builder(
    Type28Enum.ROUND_ROBIN
)
.build();
```



