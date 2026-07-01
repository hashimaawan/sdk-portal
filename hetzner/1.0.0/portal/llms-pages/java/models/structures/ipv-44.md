# Ipv 44

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRklwdjQ0

IP address (v4) and its reverse DNS entry of this Server

*This model accepts additional fields of type Object.*


# Class Name

`Ipv44`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Blocked` | `boolean` | Required | If the IP is blocked by our anti abuse dept | boolean getBlocked() | setBlocked(boolean blocked) |
| `DnsPtr` | `String` | Required | Reverse DNS PTR entry for the IPv4 addresses of this Server | String getDnsPtr() | setDnsPtr(String dnsPtr) |
| `Id` | `Integer` | Optional | ID of the Resource | Integer getId() | setId(Integer id) |
| `Ip` | `String` | Required | IP address (v4) of this Server | String getIp() | setIp(String ip) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Ipv44;
import java.io.IOException;

Ipv44 ipv44 = new Ipv44.Builder(
    false,
    "server01.example.com",
    "1.2.3.4"
)
.id(42)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



