# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkJsb2NrJTI1MjBTdG9yYWdlJTI1MjBBY3Rpb25zJTJGT3ZlcnZpZXc

Block storage actions are commands that can be given to a DigitalOcean
Block Storage Volume. An example would be detaching or attaching a volume
from a Droplet. These requests are made on the
`/v2/volumes/$VOLUME_ID/actions` endpoint.

An action object is returned. These objects hold the current status of the
requested action.


# Get instance

An instance of the `BlockStorageActionsApi` class can be accessed from the API Client.

```
BlockStorageActionsApi blockStorageActionsApi = client.BlockStorageActionsApi;
```



