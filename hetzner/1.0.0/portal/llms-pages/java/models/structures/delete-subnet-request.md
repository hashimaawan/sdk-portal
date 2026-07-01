# Delete Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkRlbGV0ZVN1Ym5ldFJlcXVlc3Q


# Class Name

`DeleteSubnetRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `IpRange` | `String` | Required | IP range of subnet to delete | String getIpRange() | setIpRange(String ipRange) |


# Example

```java
import cloud.hetzner.api.models.DeleteSubnetRequest;

DeleteSubnetRequest deleteSubnetRequest = new DeleteSubnetRequest.Builder(
    "10.0.1.0/24"
)
.build();
```



