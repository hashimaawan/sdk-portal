# Assign Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkFzc2lnblByaW1hcnlJUFJlcXVlc3Q


# Class Name

`AssignPrimaryIPRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AssigneeId` | `int` | Required | ID of a resource of type `assignee_type` | int getAssigneeId() | setAssigneeId(int assigneeId) |
| `AssigneeType` | `String` | Required, Constant | Type of resource assigning the Primary IP to<br><br>**Value**: `"server"` | String getAssigneeType() | setAssigneeType(String assigneeType) |


# Example

```java
import cloud.hetzner.api.models.AssignPrimaryIPRequest;

AssignPrimaryIPRequest assignPrimaryIPRequest = new AssignPrimaryIPRequest.Builder(
    4711,
    "server"
)
.build();
```



