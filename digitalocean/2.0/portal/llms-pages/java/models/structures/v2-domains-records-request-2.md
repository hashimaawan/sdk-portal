# V2 Domains Records Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZWNvcmRzJTI1MjBSZXF1ZXN0Mg

*This model accepts additional fields of type Object.*


# Class Name

`V2DomainsRecordsRequest2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | `String` | Required | Variable data depending on record type. For example, the "data" value for an A record would be the IPv4 address to which the domain will be mapped. For a CAA record, it would contain the domain name of the CA being granted permission to issue certificates. | String getData() | setData(String data) |
| `Flags` | `Integer` | Required | An unsigned integer between 0-255 used for CAA records. | Integer getFlags() | setFlags(Integer flags) |
| `Id` | `Integer` | Optional, Read-only | A unique identifier for each domain record. | Integer getId() | setId(Integer id) |
| `Name` | `String` | Required | The host name, alias, or service being defined by the record. | String getName() | setName(String name) |
| `Port` | `Integer` | Optional | The port for SRV records. | Integer getPort() | setPort(Integer port) |
| `Priority` | `Integer` | Optional | The priority for SRV and MX records. | Integer getPriority() | setPriority(Integer priority) |
| `Tag` | `String` | Required | The parameter tag for CAA records. Valid values are "issue", "issuewild", or "iodef" | String getTag() | setTag(String tag) |
| `Ttl` | `Integer` | Optional | This value is the time to live for the record, in seconds. This defines the time frame that clients can cache queried information before a refresh should be requested. | Integer getTtl() | setTtl(Integer ttl) |
| `Type` | `String` | Required | The type of the DNS record. For example: A, CNAME, TXT, ... | String getType() | setType(String type) |
| `Weight` | `Integer` | Optional | The weight for SRV records. | Integer getWeight() | setWeight(Integer weight) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2DomainsRecordsRequest2;
import java.io.IOException;

V2DomainsRecordsRequest2 v2DomainsRecordsRequest2 = new V2DomainsRecordsRequest2.Builder(
    "ns1.digitalocean.com",
    null,
    "@",
    null,
    "NS"
)
.id(28448429)
.port(74)
.priority(100)
.ttl(1800)
.weight(218)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



