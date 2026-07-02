# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRlJlc2VydmVkJTI1MjBJUCUyNTIwQWN0aW9ucyUyRk92ZXJ2aWV3

As of 16 June 2022, we have renamed the [Floating IP](https://docs.digitalocean.com/reference/api/api-reference/#tag/Floating-IPs)
product to Reserved IPs. The Reserved IP product's endpoints function the exact
same way as Floating IPs. The only difference is the name change throughout the
URLs and fields. For example, the `floating_ips` field is now the `reserved_ips` field.
The Floating IP endpoints will remain active until fall 2023 before being
permanently deprecated.

With the exception of the [Projects API](https://docs.digitalocean.com/reference/api/api-reference/#tag/Projects),
we will reflect this change as an additional field in the responses across the API
where the `floating_ip` field is used. For example, the Droplet metadata response
will contain the field `reserved_ips` in addition to the `floating_ips` field.
Floating IPs retrieved using the Projects API will retain the original name.

Reserved IP actions are commands that can be given to a DigitalOcean
reserved IP. These requests are made on the actions endpoint of a specific
reserved IP.

An action object is returned. These objects hold the current status of the
requested action.


# Create Instance

The instance of the `ReservedIpActionsApi` class can be created using the API Client.

```
const reservedIpActionsApi = new ReservedIpActionsApi(client);
```



