# Domain 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkRvbWFpbjE

*This model accepts additional fields of type Object.*


# Class Name

`Domain1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `IpAddress` | `String` | Optional | This optional attribute may contain an IP address. When provided, an A record will be automatically created pointing to the apex domain. | String getIpAddress() | setIpAddress(String ipAddress) |
| `Name` | `String` | Optional | The name of the domain itself. This should follow the standard domain format of domain.TLD. For instance, `example.com` is a valid domain name. | String getName() | setName(String name) |
| `Ttl` | `Integer` | Optional, Read-only | This value is the time to live for the records on this domain, in seconds. This defines the time frame that clients can cache queried information before a refresh should be requested. | Integer getTtl() | setTtl(Integer ttl) |
| `ZoneFile` | `String` | Optional, Read-only | This attribute contains the complete contents of the zone file for the selected domain. Individual domain record resources should be used to get more granular control over records. However, this attribute can also be used to get information about the SOA record, which is created automatically and is not accessible as an individual record resource. | String getZoneFile() | setZoneFile(String zoneFile) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Domain1;
import java.io.IOException;

Domain1 domain1 = new Domain1.Builder()
    .ipAddress("192.0.2.1")
    .name("example.com")
    .ttl(1800)
    .zoneFile("$ORIGIN example.com.\n$TTL 1800\nexample.com. IN SOA ns1.digitalocean.com. hostmaster.example.com. 1415982609 10800 3600 604800 1800\nexample.com. 1800 IN NS ns1.digitalocean.com.\nexample.com. 1800 IN NS ns2.digitalocean.com.\nexample.com. 1800 IN NS ns3.digitalocean.com.\nexample.com. 1800 IN A 1.2.3.4\n")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



