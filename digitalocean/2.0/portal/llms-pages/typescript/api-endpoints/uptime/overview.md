# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRlVwdGltZSUyRk92ZXJ2aWV3

[DigitalOcean Uptime Checks](https://docs.digitalocean.com/products/uptime/) provide the ability to monitor your endpoints from around the world, and alert you when they're slow, unavailable, or SSL certificates are expiring.
To interact with Uptime, you will generally send requests to the Uptime endpoint at `/v2/uptime/`.


# Create Instance

The instance of the `UptimeApi` class can be created using the API Client.

```
const uptimeApi = new UptimeApi(client);
```



