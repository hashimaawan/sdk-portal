# Remove Target Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlJlbW92ZVRhcmdldFJlcXVlc3Q


# Class Name

`RemoveTargetRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ip` | [`Ip`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. | Ip getIp() | setIp(Ip ip) |
| `LabelSelector` | [`LabelSelector12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/label-selector-12.md) | Optional | Configuration for label selector targets, required if type is `label_selector` | LabelSelector12 getLabelSelector() | setLabelSelector(LabelSelector12 labelSelector) |
| `Server` | [`Server16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/server-16.md) | Optional | Configuration for type Server, required if type is `server` | Server16 getServer() | setServer(Server16 server) |
| `Type` | [`Type29Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/type-29.md) | Required | Type of the resource | Type29Enum getType() | setType(Type29Enum type) |


# Example

```java
import cloud.hetzner.api.models.Ip;
import cloud.hetzner.api.models.LabelSelector12;
import cloud.hetzner.api.models.RemoveTargetRequest;
import cloud.hetzner.api.models.Server16;
import cloud.hetzner.api.models.Type29Enum;

RemoveTargetRequest removeTargetRequest = new RemoveTargetRequest.Builder(
    Type29Enum.IP
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
.build();
```



