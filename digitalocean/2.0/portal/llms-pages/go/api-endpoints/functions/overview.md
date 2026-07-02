# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkZ1bmN0aW9ucyUyRk92ZXJ2aWV3

[Serverless functions](https://docs.digitalocean.com/products/functions) are blocks of code that run on demand without the need to manage any infrastructure.
You can develop functions on your local machine and then deploy them to a namespace using `doctl`, the [official DigitalOcean CLI tool](https://docs.digitalocean.com/reference/doctl).

The Serverless Functions API currently only supports creating and managing namespaces.


# Get Instance

The instance of the `FunctionsApi` class can be accessed from the API Client.

```
functionsApi := client.FunctionsApi()
```



