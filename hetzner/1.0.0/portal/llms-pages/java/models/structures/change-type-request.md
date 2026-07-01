# Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNoYW5nZVR5cGVSZXF1ZXN0


# Class Name

`ChangeTypeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LoadBalancerType` | `String` | Required | ID or name of Load Balancer type the Load Balancer should migrate to | String getLoadBalancerType() | setLoadBalancerType(String loadBalancerType) |


# Example

```java
import cloud.hetzner.api.models.ChangeTypeRequest;

ChangeTypeRequest changeTypeRequest = new ChangeTypeRequest.Builder(
    "lb21"
)
.build();
```



