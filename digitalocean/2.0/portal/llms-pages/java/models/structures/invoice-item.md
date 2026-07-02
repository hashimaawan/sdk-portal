# Invoice Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkludm9pY2VJdGVt

*This model accepts additional fields of type Object.*


# Class Name

`InvoiceItem`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Amount` | `String` | Optional | Billed amount of this invoice item. Billed in USD. | String getAmount() | setAmount(String amount) |
| `Description` | `String` | Optional | Description of the invoice item. | String getDescription() | setDescription(String description) |
| `Duration` | `String` | Optional | Duration of time this invoice item was used and subsequently billed. | String getDuration() | setDuration(String duration) |
| `DurationUnit` | `String` | Optional | Unit of time for duration. | String getDurationUnit() | setDurationUnit(String durationUnit) |
| `EndTime` | `String` | Optional | Time the invoice item stopped being billed for usage. | String getEndTime() | setEndTime(String endTime) |
| `GroupDescription` | `String` | Optional | Description of the invoice item when it is a grouped set of usage, such  as DOKS or databases. | String getGroupDescription() | setGroupDescription(String groupDescription) |
| `Product` | `String` | Optional | Name of the product being billed in the invoice item. | String getProduct() | setProduct(String product) |
| `ProjectName` | `String` | Optional | Name of the DigitalOcean Project this resource belongs to. | String getProjectName() | setProjectName(String projectName) |
| `ResourceId` | `String` | Optional | ID of the resource billing in the invoice item if available. | String getResourceId() | setResourceId(String resourceId) |
| `ResourceUuid` | `String` | Optional | UUID of the resource billing in the invoice item if available. | String getResourceUuid() | setResourceUuid(String resourceUuid) |
| `StartTime` | `String` | Optional | Time the invoice item began to be billed for usage. | String getStartTime() | setStartTime(String startTime) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.InvoiceItem;
import java.io.IOException;

InvoiceItem invoiceItem = new InvoiceItem.Builder()
    .amount("12.34")
    .description("a56e086a317d8410c8b4cfd1f4dc9f82")
    .duration("744")
    .durationUnit("Hours")
    .endTime("2020-02-01T00:00:00Z")
    .groupDescription("my-doks-cluster")
    .product("Kubernetes Clusters")
    .projectName("web")
    .resourceId("2353624")
    .resourceUuid("711157cb-37c8-4817-b371-44fa3504a39c")
    .startTime("2020-01-01T00:00:00Z")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



