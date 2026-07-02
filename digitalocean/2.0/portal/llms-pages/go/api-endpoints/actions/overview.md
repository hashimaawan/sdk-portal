# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkFjdGlvbnMlMkZPdmVydmlldw

Actions are records of events that have occurred on the resources in your account.
These can be things like rebooting a Droplet, or transferring an image to a new region.

An action object is created every time one of these actions is initiated. The action
object contains information about the current status of the action, start and complete
timestamps, and the associated resource type and ID.

Every action that creates an action object is available through this endpoint. Completed
actions are not removed from this list and are always available for querying.

**Note:** You can pass the following HTTP header with the request to have the API return
the `reserved_ips` stanza instead of the `floating_ips` stanza:

- `Accept: application/vnd.digitalocean.reserveip+json`


# Get Instance

The instance of the `ActionsApi` class can be accessed from the API Client.

```
actionsApi := client.ActionsApi()
```



