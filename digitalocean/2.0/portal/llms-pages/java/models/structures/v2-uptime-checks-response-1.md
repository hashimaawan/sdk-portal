# V2 Uptime Checks Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Object.*


# Class Name

`V2UptimeChecksResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Check` | [`Check`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/check.md) | Optional | - | Check getCheck() | setCheck(Check check) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Check;
import com.digitalocean.api.models.Region8;
import com.digitalocean.api.models.V2UptimeChecksResponse1;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

V2UptimeChecksResponse1 v2UptimeChecksResponse1 = new V2UptimeChecksResponse1.Builder()
    .check(new Check.Builder()
        .id(UUID.fromString("00000c0a-0000-0000-0000-000000000000"))
        .enabled(false)
        .name("name2")
        .regions(Arrays.asList(
            Region8.SE_ASIA
        ))
        .target("target0")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



