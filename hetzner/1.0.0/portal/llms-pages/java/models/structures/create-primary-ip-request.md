# Create Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlcXVlc3Q


# Class Name

`CreatePrimaryIPRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AssigneeId` | `Integer` | Optional | ID of the resource the Primary IP should be assigned to. Omitted if it should not be assigned. | Integer getAssigneeId() | setAssigneeId(Integer assigneeId) |
| `AssigneeType` | `String` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `"server"` | String getAssigneeType() | setAssigneeType(String assigneeType) |
| `AutoDelete` | `Boolean` | Optional | Delete the Primary IP when the Server it is assigned to is deleted. If omitted defaults to `false`. | Boolean getAutoDelete() | setAutoDelete(Boolean autoDelete) |
| `Datacenter` | `String` | Optional | ID or name of Datacenter the Primary IP will be bound to. Needs to be omitted if `assignee_id` is passed. | String getDatacenter() | setDatacenter(String datacenter) |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Name` | `String` | Required | - | String getName() | setName(String name) |
| `Type` | [`Type51Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-51.md) | Required | Primary IP type | Type51Enum getType() | setType(Type51Enum type) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.CreatePrimaryIPRequest;
import cloud.hetzner.api.models.Type51Enum;
import java.io.IOException;

CreatePrimaryIPRequest createPrimaryIPRequest = new CreatePrimaryIPRequest.Builder(
    "server",
    "my-ip",
    Type51Enum.IPV4
)
.assigneeId(17)
.autoDelete(false)
.datacenter("fsn1-dc8")
.labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
.build();
```



