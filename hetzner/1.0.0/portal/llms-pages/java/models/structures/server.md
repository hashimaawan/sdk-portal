# Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcg


# Class Name

`Server`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |


# Example

```java
import cloud.hetzner.api.models.Server;

Server server = new Server.Builder(
    42
)
.build();
```



