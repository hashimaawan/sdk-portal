# Query Runtime Statistics Rows

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3NSb3dz

Statistics such as input rows and bytes read by the query, rows and bytes output by the query, and the number of rows written by the query.


# Class Name

`QueryRuntimeStatisticsRows`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `InputRows` | `Integer` | Optional | - | Integer getInputRows() | setInputRows(Integer inputRows) |
| `InputBytes` | `Integer` | Optional | - | Integer getInputBytes() | setInputBytes(Integer inputBytes) |
| `OutputBytes` | `Integer` | Optional | - | Integer getOutputBytes() | setOutputBytes(Integer outputBytes) |
| `OutputRows` | `Integer` | Optional | - | Integer getOutputRows() | setOutputRows(Integer outputRows) |


# Example

```java
import com.amazonaws.useast1.athena.models.QueryRuntimeStatisticsRows;

QueryRuntimeStatisticsRows queryRuntimeStatisticsRows = new QueryRuntimeStatisticsRows.Builder()
    .inputRows(234)
    .inputBytes(254)
    .outputBytes(40)
    .outputRows(226)
    .build();
```



