# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkRvbWFpbnMlMkZPdmVydmlldw

Domain resources are domain names that you have purchased from a domain
name registrar that you are managing through the
[DigitalOcean DNS interface](https://www.digitalocean.com/docs/networking/dns/).

This resource establishes top-level control over each domain. Actions that
affect individual domain records should be taken on the
[Domain Records](#tag/Domain-Records) resource.


# Get instance

An instance of the `DomainsApi` class can be accessed from the API Client.

```
DomainsApi domainsApi = client.DomainsApi;
```



