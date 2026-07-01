# Assign Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkFzc2lnbkZsb2F0aW5nSVBSZXF1ZXN0

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `floating_ip_assigned`        | The floating IP is already assigned                           |

*This model accepts additional fields of type Object.*


# Class Name

`AssignFloatingIpRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Server` | `int` | Required | ID of the Server the Floating IP shall be assigned to | int getServer() | setServer(int server) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.AssignFloatingIpRequest;
import java.io.IOException;

AssignFloatingIpRequest assignFloatingIpRequest = new AssignFloatingIpRequest.Builder(
    42
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



