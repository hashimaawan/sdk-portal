# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkZpcmV3YWxscyUyRk92ZXJ2aWV3

Firewalls can limit the network access to or from your resources.

* When applying a firewall with no `in` rule all inbound traffic will be dropped. The default for `in` is `DROP`.
* When applying a firewall with no `out` rule all outbound traffic will be accepted. The default for `out` is `ACCEPT`.


# Get instance

An instance of the `FirewallsController` class can be accessed from the API Client.

```
FirewallsController firewallsController = client.getFirewallsController();
```



