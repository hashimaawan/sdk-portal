# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRklTT3MlMkZPdmVydmlldw

ISOs are read-only Images of DVDs. While we recommend using our Image functionality to install your Servers we also provide some stock ISOs so you can install more exotic operating systems by yourself.

On request our support uploads a private ISO just for you. These are marked with type `private` and only visible in your Project.

To attach an ISO to your Server use `POST /servers/{id}/actions/attach_iso`.


# Get singleton instance

The singleton instance of the `IsOsApi` class can be accessed from the API Client.

```
$isOsApi = $client->getIsOsApi();
```



