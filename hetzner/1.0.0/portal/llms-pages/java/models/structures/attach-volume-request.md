# Attach Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkF0dGFjaFZvbHVtZVJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`AttachVolumeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Automount` | `Boolean` | Optional | Auto-mount the Volume after attaching it | Boolean getAutomount() | setAutomount(Boolean automount) |
| `Server` | `int` | Required | ID of the Server the Volume will be attached to | int getServer() | setServer(int server) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.AttachVolumeRequest;
import java.io.IOException;

AttachVolumeRequest attachVolumeRequest = new AttachVolumeRequest.Builder(
    43
)
.automount(false)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



