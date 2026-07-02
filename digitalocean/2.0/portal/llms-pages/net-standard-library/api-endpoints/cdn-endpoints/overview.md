# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkNETiUyNTIwRW5kcG9pbnRzJTJGT3ZlcnZpZXc

Content hosted in DigitalOcean's object storage solution,
[Spaces](https://www.digitalocean.com/docs/spaces/overview/),
can optionally be served by our globally distributed Content Delivery
Network (CDN). By sending requests to `/v2/cdn/endpoints`, you can list,
create, or delete CDN Endpoints as well as purge cached content. To use a
custom subdomain to access the CDN Endpoint, provide the ID of a
DigitalOcean managed TLS certificate and the fully qualified domain name
for the custom subdomain.


# Get instance

An instance of the `CdnEndpointsApi` class can be accessed from the API Client.

```
CdnEndpointsApi cdnEndpointsApi = client.CdnEndpointsApi;
```



