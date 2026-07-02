# A Criterion for Routing HTTP Traffic to a Component

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkElMjUyMGNyaXRlcmlvbiUyNTIwZm9yJTI1MjByb3V0aW5nJTI1MjBIVFRQJTI1MjB0cmFmZmljJTI1MjB0byUyNTIwYSUyNTIwY29tcG9uZW50Lg

*This model accepts additional fields of type Object.*


# Class Name

`ACriterionForRoutingHttpTrafficToAComponent`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Path` | `String` | Optional | An HTTP path prefix. Paths must start with / and must be unique across all components within an app. | String getPath() | setPath(String path) |
| `PreservePathPrefix` | `Boolean` | Optional | An optional flag to preserve the path that is forwarded to the backend service. By default, the HTTP request path will be trimmed from the left when forwarded to the component. For example, a component with `path=/api` will have requests to `/api/list` trimmed to `/list`. If this value is `true`, the path will remain `/api/list`. | Boolean getPreservePathPrefix() | setPreservePathPrefix(Boolean preservePathPrefix) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.ACriterionForRoutingHttpTrafficToAComponent;
import java.io.IOException;

ACriterionForRoutingHttpTrafficToAComponent aCriterionForRoutingHttpTrafficToAComponent = new ACriterionForRoutingHttpTrafficToAComponent.Builder()
    .path("/api")
    .preservePathPrefix(true)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



