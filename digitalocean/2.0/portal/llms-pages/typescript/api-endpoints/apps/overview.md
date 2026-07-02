# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkFwcHMlMkZPdmVydmlldw

App Platform is a Platform-as-a-Service (PaaS) offering from DigitalOcean that allows
developers to publish code directly to DigitalOcean servers without worrying about the
underlying infrastructure.

Most API operations are centered around a few core object types. Following are the
definitions of these types. These definitions will be omitted from the operation-specific
documentation.

For documentation on app specifications (`AppSpec` objects), please refer to the
[product documentation](https://docs.digitalocean.com/products/app-platform/reference/app-spec/)).


# Create Instance

The instance of the `AppsApi` class can be created using the API Client.

```
const appsApi = new AppsApi(client);
```



