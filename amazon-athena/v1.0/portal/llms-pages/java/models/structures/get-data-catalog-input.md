# Get Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nSW5wdXQ


# Class Name

`GetDataCatalogInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getName() | setName(String name) |


# Example

```java
import com.amazonaws.useast1.athena.models.GetDataCatalogInput;

GetDataCatalogInput getDataCatalogInput = new GetDataCatalogInput.Builder(
    "Name6"
)
.build();
```



