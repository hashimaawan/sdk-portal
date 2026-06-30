# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkltYWdlcyUyRk92ZXJ2aWV3

Images are blueprints for your VM disks. They can be of different types:

### System Images

Distribution Images maintained by us, e.g. “Ubuntu 20.04”

### Snapshot Images

Maintained by you, for example “Ubuntu 20.04 with my own settings”. These are billed per GB per month.

### Backup Images

Daily Backups of your Server. Will automatically be created for Servers which have backups enabled (`POST /servers/{id}/actions/enable_backup`)

Bound to exactly one Server. If you delete the Server, you also delete all backups bound to it. You may convert backup Images to snapshot Images to keep them.

These are billed at 20% of your instance price for 7 backup slots.

### App Images

Prebuild images with specific software configurations, e.g. “Wordpress”. All app images are created by us.


# Create Instance

The instance of the `ImagesController` class can be created using the API Client.

```
const imagesController = new ImagesController(client);
```



