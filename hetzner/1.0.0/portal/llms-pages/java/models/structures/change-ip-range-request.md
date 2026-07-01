# Change IP Range Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNoYW5nZUlQUmFuZ2VSZXF1ZXN0


# Class Name

`ChangeIPRangeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `IpRange` | `String` | Required | The new prefix for the whole Network | String getIpRange() | setIpRange(String ipRange) |


# Example

```java
import cloud.hetzner.api.models.ChangeIPRangeRequest;

ChangeIPRangeRequest changeIPRangeRequest = new ChangeIPRangeRequest.Builder(
    "10.0.0.0/12"
)
.build();
```



