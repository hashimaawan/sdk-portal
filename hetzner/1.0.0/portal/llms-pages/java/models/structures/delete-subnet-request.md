# Delete Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkRlbGV0ZVN1Ym5ldFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`DeleteSubnetRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `IpRange` | `String` | Required | IP range of subnet to delete | String getIpRange() | setIpRange(String ipRange) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.DeleteSubnetRequest;
import java.io.IOException;

DeleteSubnetRequest deleteSubnetRequest = new DeleteSubnetRequest.Builder(
    "10.0.1.0/24"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



