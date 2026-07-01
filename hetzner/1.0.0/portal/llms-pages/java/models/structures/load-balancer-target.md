# Load Balancer Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldA

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancerTarget`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `HealthStatus` | [`List<HealthStatus>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/health-status.md) | Optional | List of health statuses of the services on this target | List<HealthStatus> getHealthStatus() | setHealthStatus(List<HealthStatus> healthStatus) |
| `Ip` | [`Ip`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. | Ip getIp() | setIp(Ip ip) |
| `LabelSelector` | [`LabelSelector7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/label-selector-7.md) | Optional | Label selector and a list of selected targets | LabelSelector7 getLabelSelector() | setLabelSelector(LabelSelector7 labelSelector) |
| `Server` | [`LoadBalancerTargetServer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancer-target-server.md) | Optional | Server where the traffic should be routed through | LoadBalancerTargetServer getServer() | setServer(LoadBalancerTargetServer server) |
| `Targets` | [`List<Target>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/target.md) | Optional | List of selected targets | List<Target> getTargets() | setTargets(List<Target> targets) |
| `Type` | [`Type29`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-29.md) | Required | Type of the resource | Type29 getType() | setType(Type29 type) |
| `UsePrivateIp` | `Boolean` | Optional | Use the private network IP instead of the public IP. Default value is false. | Boolean getUsePrivateIp() | setUsePrivateIp(Boolean usePrivateIp) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.HealthStatus;
import cloud.hetzner.api.models.Ip;
import cloud.hetzner.api.models.LabelSelector7;
import cloud.hetzner.api.models.LoadBalancerTarget;
import cloud.hetzner.api.models.LoadBalancerTargetServer;
import cloud.hetzner.api.models.Server11;
import cloud.hetzner.api.models.Status30;
import cloud.hetzner.api.models.Target;
import cloud.hetzner.api.models.Type29;
import java.io.IOException;
import java.util.Arrays;

LoadBalancerTarget loadBalancerTarget = new LoadBalancerTarget.Builder(
    Type29.LABEL_SELECTOR
)
.healthStatus(Arrays.asList(
        new HealthStatus.Builder()
            .listenPort(142)
            .status(Status30.UNKNOWN)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new HealthStatus.Builder()
            .listenPort(142)
            .status(Status30.UNKNOWN)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.ip(new Ip.Builder(
        "ip8"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.labelSelector(new LabelSelector7.Builder(
        "selector8"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.server(new LoadBalancerTargetServer.Builder(
        14
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.targets(Arrays.asList(
        new Target.Builder()
            .healthStatus(Arrays.asList(
                new HealthStatus.Builder()
                    .listenPort(142)
                    .status(Status30.UNKNOWN)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                new HealthStatus.Builder()
                    .listenPort(142)
                    .status(Status30.UNKNOWN)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
            ))
            .server(new Server11.Builder(
                14
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
            .type("type2")
            .usePrivateIp(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Target.Builder()
            .healthStatus(Arrays.asList(
                new HealthStatus.Builder()
                    .listenPort(142)
                    .status(Status30.UNKNOWN)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                new HealthStatus.Builder()
                    .listenPort(142)
                    .status(Status30.UNKNOWN)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
            ))
            .server(new Server11.Builder(
                14
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
            .type("type2")
            .usePrivateIp(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Target.Builder()
            .healthStatus(Arrays.asList(
                new HealthStatus.Builder()
                    .listenPort(142)
                    .status(Status30.UNKNOWN)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                new HealthStatus.Builder()
                    .listenPort(142)
                    .status(Status30.UNKNOWN)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
            ))
            .server(new Server11.Builder(
                14
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
            .type("type2")
            .usePrivateIp(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



