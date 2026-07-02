# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRlZQQ3MlMkZPdmVydmlldw

[VPCs (virtual private clouds)](https://www.digitalocean.com/docs/networking/vpc/)
allow you to create virtual networks containing resources that can
communicate with each other in full isolation using private IP addresses.

By sending requests to the `/v2/vpcs` endpoint, you can create, configure,
list, and delete custom VPCs as well as retrieve information about the
resources assigned to them.


# Get singleton instance

The singleton instance of the `VpCsApi` class can be accessed from the API Client.

```
$vpCsApi = $client->getVpCsApi();
```



