# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkFwcHMlMkZPdmVydmlldw

App Platform is a Platform-as-a-Service (PaaS) offering from DigitalOcean that allows
developers to publish code directly to DigitalOcean servers without worrying about the
underlying infrastructure.

Most API operations are centered around a few core object types. Following are the
definitions of these types. These definitions will be omitted from the operation-specific
documentation.

For documentation on app specifications (`AppSpec` objects), please refer to the
[product documentation](https://docs.digitalocean.com/products/app-platform/reference/app-spec/)).


# Get instance

An instance of the `AppsApi` class can be accessed from the API Client.

```
AppsApi appsApi = client.getAppsApi();
```



