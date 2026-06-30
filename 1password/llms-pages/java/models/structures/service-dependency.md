# Service Dependency

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0bSUyRlNlcnZpY2VEZXBlbmRlbmN5

The state of a registered server dependency.

*This model accepts additional fields of type Object.*


# Class Name

`ServiceDependency`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Message` | `String` | Optional | Human-readable message for explaining the current state. | String getMessage() | setMessage(String message) |
| `Service` | `String` | Optional | - | String getService() | setService(String service) |
| `Status` | `String` | Optional | - | String getStatus() | setStatus(String status) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import java.io.IOException;
import local.m1password.ApiHelper;
import local.m1password.models.ServiceDependency;

ServiceDependency serviceDependency = new ServiceDependency.Builder()
    .message("message6")
    .service("service6")
    .status("status8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



