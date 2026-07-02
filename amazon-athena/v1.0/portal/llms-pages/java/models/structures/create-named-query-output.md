# Create Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZU5hbWVkUXVlcnlPdXRwdXQ


# Class Name

`CreateNamedQueryOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NamedQueryId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | String getNamedQueryId() | setNamedQueryId(String namedQueryId) |


# Example

```java
import com.amazonaws.useast1.athena.models.CreateNamedQueryOutput;

CreateNamedQueryOutput createNamedQueryOutput = new CreateNamedQueryOutput.Builder()
    .namedQueryId("NamedQueryId0")
    .build();
```



