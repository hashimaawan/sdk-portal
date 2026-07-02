# Layout

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkxheW91dA

*This model accepts additional fields of type Object.*


# Class Name

`Layout`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NumNodes` | `Integer` | Optional | - | Integer getNumNodes() | setNumNodes(Integer numNodes) |
| `Sizes` | `List<String>` | Optional, Read-only | An array of objects containing the slugs available with various node counts | List<String> getSizes() | setSizes(List<String> sizes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Layout;
import java.io.IOException;
import java.util.Arrays;

Layout layout = new Layout.Builder()
    .numNodes(1)
    .sizes(Arrays.asList(
        "db-s-1vcpu-1gb",
        "db-s-1vcpu-2gb"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



