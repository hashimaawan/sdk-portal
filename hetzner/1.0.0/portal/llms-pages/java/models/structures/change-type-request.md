# Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNoYW5nZVR5cGVSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`ChangeTypeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LoadBalancerType` | `String` | Required | ID or name of Load Balancer type the Load Balancer should migrate to | String getLoadBalancerType() | setLoadBalancerType(String loadBalancerType) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.ChangeTypeRequest;
import java.io.IOException;

ChangeTypeRequest changeTypeRequest = new ChangeTypeRequest.Builder(
    "lb21"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



