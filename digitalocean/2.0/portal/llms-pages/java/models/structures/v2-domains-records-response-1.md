# V2 Domains Records Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZWNvcmRzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type Object.*


# Class Name

`V2DomainsRecordsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DomainRecord` | [`DomainRecord`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/domain-record.md) | Optional | - | DomainRecord getDomainRecord() | setDomainRecord(DomainRecord domainRecord) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.DomainRecord;
import com.digitalocean.api.models.V2DomainsRecordsResponse1;
import java.io.IOException;

V2DomainsRecordsResponse1 v2DomainsRecordsResponse1 = new V2DomainsRecordsResponse1.Builder()
    .domainRecord(new DomainRecord.Builder(
        "A"
    )
    .data("162.10.66.0")
    .flags(null)
    .id(28448433)
    .name("www")
    .port(null)
    .priority(null)
    .tag(null)
    .ttl(1800)
    .weight(null)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



