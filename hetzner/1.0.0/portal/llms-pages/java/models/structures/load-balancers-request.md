# Load Balancers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancersRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Name` | `String` | Optional | New Load Balancer name | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.LoadBalancersRequest;
import java.io.IOException;

LoadBalancersRequest loadBalancersRequest = new LoadBalancersRequest.Builder()
    .labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
    .name("new-name")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



