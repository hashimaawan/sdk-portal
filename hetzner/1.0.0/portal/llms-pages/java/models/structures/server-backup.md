# Server Backup

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlckJhY2t1cA

Will increase base Server costs by specific percentage


# Class Name

`ServerBackup`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Percentage` | `String` | Required | Percentage by how much the base price will increase | String getPercentage() | setPercentage(String percentage) |


# Example

```java
import cloud.hetzner.api.models.ServerBackup;

ServerBackup serverBackup = new ServerBackup.Builder(
    "20.0000000000"
)
.build();
```



