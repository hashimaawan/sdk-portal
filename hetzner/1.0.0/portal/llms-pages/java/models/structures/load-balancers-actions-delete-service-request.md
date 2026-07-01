# Load Balancers Actions Delete Service Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGVsZXRlJTI1MjBTZXJ2aWNlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancersActionsDeleteServiceRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ListenPort` | `double` | Required | The listen port of the service you want to delete | double getListenPort() | setListenPort(double listenPort) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.LoadBalancersActionsDeleteServiceRequest;
import java.io.IOException;

LoadBalancersActionsDeleteServiceRequest loadBalancersActionsDeleteServiceRequest = new LoadBalancersActionsDeleteServiceRequest.Builder(
    4711D
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



