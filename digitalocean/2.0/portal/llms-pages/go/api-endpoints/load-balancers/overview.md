# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRk92ZXJ2aWV3

[DigitalOcean Load Balancers](https://www.digitalocean.com/docs/networking/load-balancers/)
provide a way to distribute traffic across multiple Droplets. By sending
requests to the `/v2/load_balancers` endpoint, you can list, create, or
delete load balancers as well as add or remove Droplets, forwarding rules,
and other configuration details.


# Get Instance

The instance of the `LoadBalancersApi` class can be accessed from the API Client.

```
loadBalancersApi := client.LoadBalancersApi()
```



