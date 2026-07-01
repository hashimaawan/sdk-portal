# Change DNSPTR Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNoYW5nZUROU1BUUlJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`ChangeDnsptrRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DnsPtr` | `String` | Required | Hostname to set as a reverse DNS PTR entry, will reset to original default value if `null` | String getDnsPtr() | setDnsPtr(String dnsPtr) |
| `Ip` | `String` | Required | IP address for which to set the reverse DNS entry | String getIp() | setIp(String ip) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.ChangeDnsptrRequest;
import java.io.IOException;

ChangeDnsptrRequest changeDnsptrRequest = new ChangeDnsptrRequest.Builder(
    "server02.example.com",
    "1.2.3.4"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



