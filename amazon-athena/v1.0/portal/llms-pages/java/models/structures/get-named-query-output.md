# Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlPdXRwdXQ


# Class Name

`GetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NamedQuery` | [`NamedQuery1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/named-query-1.md) | Optional | - | NamedQuery1 getNamedQuery() | setNamedQuery(NamedQuery1 namedQuery) |


# Example

```java
import com.amazonaws.useast1.athena.models.GetNamedQueryOutput;
import com.amazonaws.useast1.athena.models.NamedQuery1;

GetNamedQueryOutput getNamedQueryOutput = new GetNamedQueryOutput.Builder()
    .namedQuery(new NamedQuery1.Builder(
        "Name0",
        "Database8",
        "QueryString2"
    )
    .description("Description6")
    .namedQueryId("NamedQueryId2")
    .workGroup("WorkGroup2")
    .build())
    .build();
```



