# Assign Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkFzc2lnblByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`AssignPrimaryIpRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AssigneeId` | `int` | Required | ID of a resource of type `assignee_type` | int getAssigneeId() | setAssigneeId(int assigneeId) |
| `AssigneeType` | `String` | Required, Constant | Type of resource assigning the Primary IP to<br><br>**Value**: `"server"` | String getAssigneeType() | setAssigneeType(String assigneeType) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.AssignPrimaryIpRequest;
import java.io.IOException;

AssignPrimaryIpRequest assignPrimaryIpRequest = new AssignPrimaryIpRequest.Builder(
    4711,
    "server"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



