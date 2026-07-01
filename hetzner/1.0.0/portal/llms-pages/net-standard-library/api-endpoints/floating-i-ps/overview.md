# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZPdmVydmlldw

Floating IPs help you to create highly available setups. You can assign a Floating IP to any Server. The Server can then use this IP. You can reassign it to a different Server at any time, or you can choose to unassign the IP from Servers all together.

Floating IPs can be used globally. This means you can assign a Floating IP to a Server in one Location and later reassign it to a Server in a different Location. For optimal routing and latency Floating IPs should be used in the Location they were created in.

For Floating IPs to work with your Server, you must configure them inside your operation system.

Floating IPs of type `ipv4` use a single IPv4 address as their `ip` property. Floating IPs of type `ipv6` use a /64 network such as `fc00::/64` as their `ip` property. Any IP address within that network can be used on your host.

Floating IPs are billed on a monthly basis.


# Get instance

An instance of the `FloatingIPsController` class can be accessed from the API Client.

```
FloatingIPsController floatingIPsController = client.FloatingIPsController;
```



