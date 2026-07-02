# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRlRhZ3MlMkZPdmVydmlldw

A tag is a label that can be applied to a resource (currently Droplets,
Images, Volumes, Volume Snapshots, and Database clusters) in order to
better organize or facilitate the lookups and actions on it.

Tags have two attributes: a user defined `name` attribute and an embedded
`resources` attribute with information about resources that have been tagged.


# Get instance

An instance of the `TagsApi` class can be accessed from the API Client.

```
tags_api = client.tags
```



