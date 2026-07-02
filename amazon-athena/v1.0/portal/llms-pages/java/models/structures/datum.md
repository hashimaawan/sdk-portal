# Datum

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkRhdHVt

A piece of data (a field in the table).


# Class Name

`Datum`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `VarCharValue` | `String` | Optional | - | String getVarCharValue() | setVarCharValue(String varCharValue) |


# Example

```java
import com.amazonaws.useast1.athena.models.Datum;

Datum datum = new Datum.Builder()
    .varCharValue("VarCharValue8")
    .build();
```



