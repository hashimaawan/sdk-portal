# Create Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkNyZWF0ZVNlcnZlclJlcXVlc3Q


# Class Name

`CreateServerRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Automount` | `Boolean` | Optional | Auto-mount Volumes after attach | Boolean getAutomount() | setAutomount(Boolean automount) |
| `Datacenter` | `String` | Optional | ID or name of Datacenter to create Server in (must not be used together with location) | String getDatacenter() | setDatacenter(String datacenter) |
| `Firewalls` | [`List<Firewall4>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/firewall-4.md) | Optional | Firewalls which should be applied on the Server's public network interface at creation time | List<Firewall4> getFirewalls() | setFirewalls(List<Firewall4> firewalls) |
| `Image` | `String` | Required | ID or name of the Image the Server is created from | String getImage() | setImage(String image) |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Location` | `String` | Optional | ID or name of Location to create Server in (must not be used together with datacenter) | String getLocation() | setLocation(String location) |
| `Name` | `String` | Required | Name of the Server to create (must be unique per Project and a valid hostname as per RFC 1123) | String getName() | setName(String name) |
| `Networks` | `List<Integer>` | Optional | Network IDs which should be attached to the Server private network interface at the creation time | List<Integer> getNetworks() | setNetworks(List<Integer> networks) |
| `PlacementGroup` | `Integer` | Optional | ID of the Placement Group the server should be in | Integer getPlacementGroup() | setPlacementGroup(Integer placementGroup) |
| `PublicNet` | [`PublicNet5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/public-net-5.md) | Optional | Public Network options | PublicNet5 getPublicNet() | setPublicNet(PublicNet5 publicNet) |
| `ServerType` | `String` | Required | ID or name of the Server type this Server should be created with | String getServerType() | setServerType(String serverType) |
| `SshKeys` | `List<String>` | Optional | SSH key IDs (`integer`) or names (`string`) which should be injected into the Server at creation time | List<String> getSshKeys() | setSshKeys(List<String> sshKeys) |
| `StartAfterCreate` | `Boolean` | Optional | Start Server right after creation. Defaults to true. | Boolean getStartAfterCreate() | setStartAfterCreate(Boolean startAfterCreate) |
| `UserData` | `String` | Optional | Cloud-Init user data to use during Server creation. This field is limited to 32KiB. | String getUserData() | setUserData(String userData) |
| `Volumes` | `List<Integer>` | Optional | Volume IDs which should be attached to the Server at the creation time. Volumes must be in the same Location. | List<Integer> getVolumes() | setVolumes(List<Integer> volumes) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.CreateServerRequest;
import cloud.hetzner.api.models.Firewall4;
import java.io.IOException;
import java.util.Arrays;

CreateServerRequest createServerRequest = new CreateServerRequest.Builder(
    "ubuntu-20.04",
    "my-server",
    "cx11"
)
.automount(false)
.datacenter("nbg1-dc3")
.firewalls(Arrays.asList(
        new Firewall4.Builder()
            .firewall(38)
            .build()
    ))
.labels(ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.location("nbg1")
.networks(Arrays.asList(
        456
    ))
.placementGroup(1)
.sshKeys(Arrays.asList(
        "my-ssh-key"
    ))
.startAfterCreate(true)
.userData("#cloud-config\nruncmd:\n- [touch, /root/cloud-init-worked]\n")
.volumes(Arrays.asList(
        123
    ))
.build();
```



