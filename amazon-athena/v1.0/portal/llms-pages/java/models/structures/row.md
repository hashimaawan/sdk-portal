# Row

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlJvdw

The rows that make up a query result table.


# Class Name

`Row`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`List<Datum>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/datum.md) | Optional | - | List<Datum> getData() | setData(List<Datum> data) |


# Example

```java
import com.amazonaws.useast1.athena.models.Datum;
import com.amazonaws.useast1.athena.models.Row;
import java.util.Arrays;

Row row = new Row.Builder()
    .data(Arrays.asList(
        new Datum.Builder()
            .varCharValue("VarCharValue8")
            .build()
    ))
    .build();
```



