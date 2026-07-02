# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkltYWdlJTI1MjBBY3Rpb25zJTJGT3ZlcnZpZXc

Image actions are commands that can be given to a DigitalOcean image. In
general, these requests are made on the actions endpoint of a specific
image.

An image action object is returned. These objects hold the current status
of the requested action.


# Get Instance

The instance of the `ImageActionsApi` class can be accessed from the API Client.

```
imageActionsApi := client.ImageActionsApi()
```



