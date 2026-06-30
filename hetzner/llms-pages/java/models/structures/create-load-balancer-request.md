# Create Load Balancer Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkNyZWF0ZUxvYWRCYWxhbmNlclJlcXVlc3Q


# Class Name

`CreateLoadBalancerRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Algorithm` | [`LoadBalancerAlgorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/load-balancer-algorithm.md) | Required | Algorithm of the Load Balancer | LoadBalancerAlgorithm getAlgorithm() | setAlgorithm(LoadBalancerAlgorithm algorithm) |
| `Labels` | [`Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) | Labels getLabels() | setLabels(Labels labels) |
| `LoadBalancerType` | `String` | Required | ID or name of the Load Balancer type this Load Balancer should be created with | String getLoadBalancerType() | setLoadBalancerType(String loadBalancerType) |
| `Location` | `String` | Optional | ID or name of Location to create Load Balancer in | String getLocation() | setLocation(String location) |
| `Name` | `String` | Required | Name of the Load Balancer | String getName() | setName(String name) |
| `Network` | `Integer` | Optional | ID of the network the Load Balancer should be attached to on creation | Integer getNetwork() | setNetwork(Integer network) |
| `NetworkZone` | `String` | Optional | Name of network zone | String getNetworkZone() | setNetworkZone(String networkZone) |
| `PublicInterface` | `Boolean` | Optional | Enable or disable the public interface of the Load Balancer | Boolean getPublicInterface() | setPublicInterface(Boolean publicInterface) |
| `Services` | [`List<LoadBalancerService>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/load-balancer-service.md) | Optional | Array of services | List<LoadBalancerService> getServices() | setServices(List<LoadBalancerService> services) |
| `Targets` | [`List<LoadBalancerTarget>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/load-balancer-target.md) | Optional | Array of targets | List<LoadBalancerTarget> getTargets() | setTargets(List<LoadBalancerTarget> targets) |


# Example

```java
import cloud.hetzner.api.models.CreateLoadBalancerRequest;
import cloud.hetzner.api.models.Labels;
import cloud.hetzner.api.models.LoadBalancerAlgorithm;
import cloud.hetzner.api.models.Type28Enum;

CreateLoadBalancerRequest createLoadBalancerRequest = new CreateLoadBalancerRequest.Builder(
    new LoadBalancerAlgorithm.Builder(
        Type28Enum.ROUND_ROBIN
    )
    .build(),
    "lb11",
    "Web Frontend"
)
.labels(new Labels.Builder()
        .labelkey("labelkey4")
        .build())
.location("location2")
.network(123)
.networkZone("eu-central")
.publicInterface(true)
.build();
```



