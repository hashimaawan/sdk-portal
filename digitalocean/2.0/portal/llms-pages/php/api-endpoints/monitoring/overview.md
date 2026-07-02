# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRk1vbml0b3JpbmclMkZPdmVydmlldw

The DigitalOcean Monitoring API makes it possible to programmatically retrieve metrics as well as configure alert
policies based on these metrics. The Monitoring API can help you gain insight into how your apps are performing
and consuming resources.


# Get singleton instance

The singleton instance of the `MonitoringApi` class can be accessed from the API Client.

```
$monitoringApi = $client->getMonitoringApi();
```



