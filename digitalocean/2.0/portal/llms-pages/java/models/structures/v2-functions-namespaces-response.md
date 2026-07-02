# V2 Functions Namespaces Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2FunctionsNamespacesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Namespaces` | [`List<Namespace>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/namespace.md) | Optional | - | List<Namespace> getNamespaces() | setNamespaces(List<Namespace> namespaces) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Namespace;
import com.digitalocean.api.models.V2FunctionsNamespacesResponse;
import java.io.IOException;
import java.util.Arrays;

V2FunctionsNamespacesResponse v2FunctionsNamespacesResponse = new V2FunctionsNamespacesResponse.Builder()
    .namespaces(Arrays.asList(
        new Namespace.Builder()
            .apiHost("api_host8")
            .createdAt("created_at0")
            .key("key2")
            .label("label2")
            .namespace("namespace0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Namespace.Builder()
            .apiHost("api_host8")
            .createdAt("created_at0")
            .key("key2")
            .label("label2")
            .namespace("namespace0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



