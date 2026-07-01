# Add Target Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkFkZFRhcmdldFJlcXVlc3Q


# Class Name

`AddTargetRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ip` | [`Ip`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. | Ip getIp() | setIp(Ip ip) |
| `LabelSelector` | [`LabelSelector12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/label-selector-12.md) | Optional | Configuration for label selector targets, required if type is `label_selector` | LabelSelector12 getLabelSelector() | setLabelSelector(LabelSelector12 labelSelector) |
| `Server` | [`Server16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server-16.md) | Optional | Configuration for type Server, required if type is `server` | Server16 getServer() | setServer(Server16 server) |
| `Type` | [`Type29Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-29.md) | Required | Type of the resource | Type29Enum getType() | setType(Type29Enum type) |
| `UsePrivateIp` | `Boolean` | Optional | Use the private network IP instead of the public IP of the Server, requires the Server and Load Balancer to be in the same network. Default value is false. | Boolean getUsePrivateIp() | setUsePrivateIp(Boolean usePrivateIp) |


# Example

```java
import cloud.hetzner.api.models.AddTargetRequest;
import cloud.hetzner.api.models.Ip;
import cloud.hetzner.api.models.LabelSelector12;
import cloud.hetzner.api.models.Server16;
import cloud.hetzner.api.models.Type29Enum;

AddTargetRequest addTargetRequest = new AddTargetRequest.Builder(
    Type29Enum.SERVER
)
.ip(new Ip.Builder(
        "ip8"
    )
    .build())
.labelSelector(new LabelSelector12.Builder(
        "selector8"
    )
    .build())
.server(new Server16.Builder(
        217.74D
    )
    .build())
.usePrivateIp(true)
.build();
```



