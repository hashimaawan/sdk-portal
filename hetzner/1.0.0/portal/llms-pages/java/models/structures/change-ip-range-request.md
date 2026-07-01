# Change IP Range Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNoYW5nZUlQUmFuZ2VSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`ChangeIpRangeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `IpRange` | `String` | Required | The new prefix for the whole Network | String getIpRange() | setIpRange(String ipRange) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.ChangeIpRangeRequest;
import java.io.IOException;

ChangeIpRangeRequest changeIpRangeRequest = new ChangeIpRangeRequest.Builder(
    "10.0.0.0/12"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



