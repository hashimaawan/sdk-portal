# V2 Functions Namespaces Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`V2FunctionsNamespacesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Label` | `String` | Required | The namespace's unique name. | String getLabel() | setLabel(String label) |
| `Region` | `String` | Required | The [datacenter region](https://docs.digitalocean.com/products/platform/availability-matrix/#available-datacenters) in which to create the namespace. | String getRegion() | setRegion(String region) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2FunctionsNamespacesRequest;
import java.io.IOException;

V2FunctionsNamespacesRequest v2FunctionsNamespacesRequest = new V2FunctionsNamespacesRequest.Builder(
    "my namespace",
    "nyc1"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



