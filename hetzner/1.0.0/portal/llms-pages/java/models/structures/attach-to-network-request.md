# Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkF0dGFjaFRvTmV0d29ya1JlcXVlc3Q


# Class Name

`AttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AliasIps` | `List<String>` | Optional | Additional IPs to be assigned to this Server | List<String> getAliasIps() | setAliasIps(List<String> aliasIps) |
| `Ip` | `String` | Optional | IP to request to be assigned to this Server; if you do not provide this then you will be auto assigned an IP address | String getIp() | setIp(String ip) |
| `Network` | `int` | Required | ID of an existing network to attach the Server to | int getNetwork() | setNetwork(int network) |


# Example

```java
import cloud.hetzner.api.models.AttachToNetworkRequest;
import java.util.Arrays;

AttachToNetworkRequest attachToNetworkRequest = new AttachToNetworkRequest.Builder(
    4711
)
.aliasIps(Arrays.asList(
        "10.0.1.2"
    ))
.ip("10.0.1.1")
.build();
```



