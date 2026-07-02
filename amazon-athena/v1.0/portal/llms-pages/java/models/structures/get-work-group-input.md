# Get Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldFdvcmtHcm91cElucHV0


# Class Name

`GetWorkGroupInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `WorkGroup` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |


# Example

```java
import com.amazonaws.useast1.athena.models.GetWorkGroupInput;

GetWorkGroupInput getWorkGroupInput = new GetWorkGroupInput.Builder(
    "WorkGroup8"
)
.build();
```



