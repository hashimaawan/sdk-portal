# Delete Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkRlbGV0ZVdvcmtHcm91cElucHV0


# Class Name

`DeleteWorkGroupInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `WorkGroup` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `RecursiveDeleteOption` | `Boolean` | Optional | - | Boolean getRecursiveDeleteOption() | setRecursiveDeleteOption(Boolean recursiveDeleteOption) |


# Example

```java
import com.amazonaws.useast1.athena.models.DeleteWorkGroupInput;

DeleteWorkGroupInput deleteWorkGroupInput = new DeleteWorkGroupInput.Builder(
    "WorkGroup0"
)
.recursiveDeleteOption(false)
.build();
```



