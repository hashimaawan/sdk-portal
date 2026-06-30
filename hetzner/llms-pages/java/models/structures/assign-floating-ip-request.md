# Assign Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkFzc2lnbkZsb2F0aW5nSVBSZXF1ZXN0

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `floating_ip_assigned`        | The floating IP is already assigned                           |


# Class Name

`AssignFloatingIPRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Server` | `int` | Required | ID of the Server the Floating IP shall be assigned to | int getServer() | setServer(int server) |


# Example

```java
import cloud.hetzner.api.models.AssignFloatingIPRequest;

AssignFloatingIPRequest assignFloatingIPRequest = new AssignFloatingIPRequest.Builder(
    42
)
.build();
```



