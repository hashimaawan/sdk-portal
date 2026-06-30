# Health Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0bSUyRkhlYWx0aCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`HealthResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Dependencies` | [`List<ServiceDependency>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/structures/service-dependency.md) | Optional | - | List<ServiceDependency> getDependencies() | setDependencies(List<ServiceDependency> dependencies) |
| `Name` | `String` | Required | - | String getName() | setName(String name) |
| `Version` | `String` | Required | The Connect server's version | String getVersion() | setVersion(String version) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import java.io.IOException;
import java.util.Arrays;
import local.m1password.ApiHelper;
import local.m1password.models.HealthResponse;
import local.m1password.models.ServiceDependency;

HealthResponse healthResponse = new HealthResponse.Builder(
    "name4",
    "version0"
)
.dependencies(Arrays.asList(
        new ServiceDependency.Builder()
            .message("message6")
            .service("service6")
            .status("status8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



