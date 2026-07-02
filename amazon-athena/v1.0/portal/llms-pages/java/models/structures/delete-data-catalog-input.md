# Delete Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkRlbGV0ZURhdGFDYXRhbG9nSW5wdXQ


# Class Name

`DeleteDataCatalogInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getName() | setName(String name) |


# Example

```java
import com.amazonaws.useast1.athena.models.DeleteDataCatalogInput;

DeleteDataCatalogInput deleteDataCatalogInput = new DeleteDataCatalogInput.Builder(
    "Name2"
)
.build();
```



