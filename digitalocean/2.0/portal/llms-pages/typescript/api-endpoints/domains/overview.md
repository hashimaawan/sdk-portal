# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkRvbWFpbnMlMkZPdmVydmlldw

Domain resources are domain names that you have purchased from a domain
name registrar that you are managing through the
[DigitalOcean DNS interface](https://www.digitalocean.com/docs/networking/dns/).

This resource establishes top-level control over each domain. Actions that
affect individual domain records should be taken on the
[Domain Records](#tag/Domain-Records) resource.


# Create Instance

The instance of the `DomainsApi` class can be created using the API Client.

```
const domainsApi = new DomainsApi(client);
```



