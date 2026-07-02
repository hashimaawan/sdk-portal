# Get Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlJbnB1dA


# Class Name

`GetNamedQueryInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NamedQueryId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | String getNamedQueryId() | setNamedQueryId(String namedQueryId) |


# Example

```java
import com.amazonaws.useast1.athena.models.GetNamedQueryInput;

GetNamedQueryInput getNamedQueryInput = new GetNamedQueryInput.Builder(
    "NamedQueryId8"
)
.build();
```



