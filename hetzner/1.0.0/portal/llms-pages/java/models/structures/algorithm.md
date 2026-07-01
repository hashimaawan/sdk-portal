# Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkFsZ29yaXRobQ

Algorithm of the Load Balancer

*This model accepts additional fields of type Object.*


# Class Name

`Algorithm`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type28`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-28.md) | Required | Type of the algorithm | Type28 getType() | setType(Type28 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Algorithm;
import cloud.hetzner.api.models.Type28;
import java.io.IOException;

Algorithm algorithm = new Algorithm.Builder(
    Type28.ROUND_ROBIN
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



