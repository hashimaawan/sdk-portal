# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRlVwdGltZSUyRk92ZXJ2aWV3

[DigitalOcean Uptime Checks](https://docs.digitalocean.com/products/uptime/) provide the ability to monitor your endpoints from around the world, and alert you when they're slow, unavailable, or SSL certificates are expiring.
To interact with Uptime, you will generally send requests to the Uptime endpoint at `/v2/uptime/`.


# Get instance

An instance of the `UptimeApi` class can be accessed from the API Client.

```
uptime_api = client.uptime
```



