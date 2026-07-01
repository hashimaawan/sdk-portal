# Servers Actions Change Dns Ptr Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwRG5zJTI1MjBQdHIlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`ServersActionsChangeDnsPtrRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DnsPtr` | `String` | Required | Hostname to set as a reverse DNS PTR entry, reset to original value if `null` | String getDnsPtr() | setDnsPtr(String dnsPtr) |
| `Ip` | `String` | Required | Primary IP address for which the reverse DNS entry should be set | String getIp() | setIp(String ip) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.ServersActionsChangeDnsPtrRequest;
import java.io.IOException;

ServersActionsChangeDnsPtrRequest serversActionsChangeDnsPtrRequest = new ServersActionsChangeDnsPtrRequest.Builder(
    "server01.example.com",
    "1.2.3.4"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



