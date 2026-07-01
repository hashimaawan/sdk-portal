# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkZpcmV3YWxscyUyRk92ZXJ2aWV3

Firewalls can limit the network access to or from your resources.

* When applying a firewall with no `in` rule all inbound traffic will be dropped. The default for `in` is `DROP`.
* When applying a firewall with no `out` rule all outbound traffic will be accepted. The default for `out` is `ACCEPT`.


# Create Instance

The instance of the `FirewallsApi` class can be created using the API Client.

```
const firewallsApi = new FirewallsApi(client);
```



