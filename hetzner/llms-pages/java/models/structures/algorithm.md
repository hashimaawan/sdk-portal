# Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkFsZ29yaXRobQ

Algorithm of the Load Balancer


# Class Name

`Algorithm`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type28Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/type-28.md) | Required | Type of the algorithm | Type28Enum getType() | setType(Type28Enum type) |


# Example

```java
import cloud.hetzner.api.models.Algorithm;
import cloud.hetzner.api.models.Type28Enum;

Algorithm algorithm = new Algorithm.Builder(
    Type28Enum.ROUND_ROBIN
)
.build();
```



