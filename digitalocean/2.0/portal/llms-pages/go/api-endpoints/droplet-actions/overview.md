# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkRyb3BsZXQlMjUyMEFjdGlvbnMlMkZPdmVydmlldw

Droplet actions are tasks that can be executed on a Droplet. These can be
things like rebooting, resizing, snapshotting, etc.

Droplet action requests are generally targeted at one of the "actions"
endpoints for a specific Droplet. The specific actions are usually
initiated by sending a POST request with the action and arguments as
parameters.

Droplet action requests create a Droplet actions object, which can be used
to get information about the status of an action. Creating a Droplet
action is asynchronous: the HTTP call will return the action object before
the action has finished processing on the Droplet. The current status of
an action can be retrieved from either the Droplet actions endpoint or the
global actions endpoint. If a Droplet action is uncompleted it may block
the creation of a subsequent action for that Droplet, the locked attribute
of the Droplet will be true and attempts to create a Droplet action will
fail with a status of 422.


# Get Instance

The instance of the `DropletActionsApi` class can be accessed from the API Client.

```
dropletActionsApi := client.DropletActionsApi()
```



