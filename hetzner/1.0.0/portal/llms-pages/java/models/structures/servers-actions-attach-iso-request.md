# Servers Actions Attach Iso Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEF0dGFjaCUyNTIwSXNvJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`ServersActionsAttachIsoRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Iso` | `String` | Required | ID or name of ISO to attach to the Server as listed in GET `/isos` | String getIso() | setIso(String iso) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.ServersActionsAttachIsoRequest;
import java.io.IOException;

ServersActionsAttachIsoRequest serversActionsAttachIsoRequest = new ServersActionsAttachIsoRequest.Builder(
    "FreeBSD-11.0-RELEASE-amd64-dvd1"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



