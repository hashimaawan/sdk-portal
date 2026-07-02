# Multiple Droplet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk11bHRpcGxlJTI1MjBEcm9wbGV0JTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`MultipleDropletRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Names` | `List<String>` | Required | An array of human human-readable strings you wish to use when displaying the Droplet name. Each name, if set to a domain name managed in the DigitalOcean DNS management system, will configure a PTR record for the Droplet. Each name set during creation will also determine the hostname for the Droplet in its internal configuration. | List<String> getNames() | setNames(List<String> names) |
| `Backups` | `Boolean` | Optional | A boolean indicating whether automated backups should be enabled for the Droplet.<br><br>**Default**: `false` | Boolean getBackups() | setBackups(Boolean backups) |
| `Image` | [`MultipleDropletRequestImage`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/oneof-anyof-definitions/multiple-droplet-request-image.md) | Required | This is a container for one-of cases. | MultipleDropletRequestImage getImage() | setImage(MultipleDropletRequestImage image) |
| `Ipv6` | `Boolean` | Optional | A boolean indicating whether to enable IPv6 on the Droplet.<br><br>**Default**: `false` | Boolean getIpv6() | setIpv6(Boolean ipv6) |
| `Monitoring` | `Boolean` | Optional | A boolean indicating whether to install the DigitalOcean agent for monitoring.<br><br>**Default**: `false` | Boolean getMonitoring() | setMonitoring(Boolean monitoring) |
| `PrivateNetworking` | `Boolean` | Optional | This parameter has been deprecated. Use `vpc_uuid` instead to specify a VPC network for the Droplet. If no `vpc_uuid` is provided, the Droplet will be placed in your account's default VPC for the region.<br><br>**Default**: `false` | Boolean getPrivateNetworking() | setPrivateNetworking(Boolean privateNetworking) |
| `Region` | `String` | Optional | The slug identifier for the region that you wish to deploy the Droplet in. If the specific datacenter is not not important, a slug prefix (e.g. `nyc`) can be used to deploy the Droplet in any of the that region's locations (`nyc1`, `nyc2`, or `nyc3`). If the region is omitted from the create request completely, the Droplet may deploy in any region. | String getRegion() | setRegion(String region) |
| `Size` | `String` | Required | The slug identifier for the size that you wish to select for this Droplet. | String getSize() | setSize(String size) |
| `SshKeys` | [`List<MultipleDropletRequestSshKeys>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/oneof-anyof-definitions/multiple-droplet-request-ssh-keys.md) | Optional | This is List of a container for any-of cases. | List<MultipleDropletRequestSshKeys> getSshKeys() | setSshKeys(List<MultipleDropletRequestSshKeys> sshKeys) |
| `Tags` | `List<String>` | Optional | A flat array of tag names as strings to apply to the Droplet after it is created. Tag names can either be existing or new tags. | List<String> getTags() | setTags(List<String> tags) |
| `UserData` | `String` | Optional | A string containing 'user data' which may be used to configure the Droplet on first boot, often a 'cloud-config' file or Bash script. It must be plain text and may not exceed 64 KiB in size. | String getUserData() | setUserData(String userData) |
| `Volumes` | `List<String>` | Optional | An array of IDs for block storage volumes that will be attached to the Droplet once created. The volumes must not already be attached to an existing Droplet. | List<String> getVolumes() | setVolumes(List<String> volumes) |
| `VpcUuid` | `String` | Optional | A string specifying the UUID of the VPC to which the Droplet will be assigned. If excluded, the Droplet will be assigned to your account's default VPC for the region. | String getVpcUuid() | setVpcUuid(String vpcUuid) |
| `WithDropletAgent` | `Boolean` | Optional | A boolean indicating whether to install the DigitalOcean agent used for providing access to the Droplet web console in the control panel. By default, the agent is installed on new Droplets but installation errors (i.e. OS not supported) are ignored. To prevent it from being installed, set to `false`. To make installation errors fatal, explicitly set it to `true`. | Boolean getWithDropletAgent() | setWithDropletAgent(Boolean withDropletAgent) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.MultipleDropletRequest;
import com.digitalocean.api.models.containers.MultipleDropletRequestImage;
import com.digitalocean.api.models.containers.MultipleDropletRequestSshKeys;
import java.io.IOException;
import java.util.Arrays;

MultipleDropletRequest multipleDropletRequest = new MultipleDropletRequest.Builder(
    Arrays.asList(
        "sub-01.example.com",
        "sub-02.example.com"
    ),
    MultipleDropletRequestImage.fromString(
        "ubuntu-20-04-x64"
    ),
    "s-1vcpu-1gb"
)
.backups(true)
.ipv6(true)
.monitoring(true)
.privateNetworking(true)
.region("nyc3")
.sshKeys(Arrays.asList(
        ,
        
    ))
.tags(Arrays.asList(
        "env:prod",
        "web"
    ))
.userData("#cloud-config\nruncmd:\n  - touch /test.txt\n")
.volumes(Arrays.asList(
        "12e97116-7280-11ed-b3d0-0a58ac146812"
    ))
.vpcUuid("760e09ef-dc84-11e8-981e-3cfdfeaae000")
.withDropletAgent(true)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



