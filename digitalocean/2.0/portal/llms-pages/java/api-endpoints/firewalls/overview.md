# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkZpcmV3YWxscyUyRk92ZXJ2aWV3

[DigitalOcean Cloud Firewalls](https://www.digitalocean.com/docs/networking/firewalls/)
provide the ability to restrict network access to and from a Droplet
allowing you to define which ports will accept inbound or outbound
connections. By sending requests to the `/v2/firewalls` endpoint, you can
list, create, or delete firewalls as well as modify access rules.


# Get instance

An instance of the `FirewallsApi` class can be accessed from the API Client.

```
FirewallsApi firewallsApi = client.getFirewallsApi();
```



