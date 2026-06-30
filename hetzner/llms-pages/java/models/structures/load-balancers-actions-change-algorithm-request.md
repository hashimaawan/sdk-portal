# Load Balancers Actions Change Algorithm Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBBbGdvcml0aG0lMjUyMFJlcXVlc3Q


# Class Name

`LoadBalancersActionsChangeAlgorithmRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type39Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/type-39.md) | Required | Algorithm of the Load Balancer | Type39Enum getType() | setType(Type39Enum type) |


# Example

```java
import cloud.hetzner.api.models.LoadBalancersActionsChangeAlgorithmRequest;
import cloud.hetzner.api.models.Type39Enum;

LoadBalancersActionsChangeAlgorithmRequest loadBalancersActionsChangeAlgorithmRequest = new LoadBalancersActionsChangeAlgorithmRequest.Builder(
    Type39Enum.ROUND_ROBIN
)
.build();
```



