# Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkRldGFjaEZyb21OZXR3b3JrUmVxdWVzdA


# Class Name

`DetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Network` | `int` | Required | ID of an existing network to detach the Server from | int getNetwork() | setNetwork(int network) |


# Example

```java
import cloud.hetzner.api.models.DetachFromNetworkRequest;

DetachFromNetworkRequest detachFromNetworkRequest = new DetachFromNetworkRequest.Builder(
    4711
)
.build();
```



