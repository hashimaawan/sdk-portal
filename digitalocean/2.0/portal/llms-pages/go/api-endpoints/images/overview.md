# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkltYWdlcyUyRk92ZXJ2aWV3

A DigitalOcean [image](https://www.digitalocean.com/docs/images/) can be
used to create a Droplet and may come in a number of flavors. Currently,
there are five types of images: snapshots, backups, applications,
distributions, and custom images.

* [Snapshots](https://www.digitalocean.com/docs/images/snapshots/) provide
  a full copy of an existing Droplet instance taken on demand.

* [Backups](https://www.digitalocean.com/docs/images/backups/) are similar
  to snapshots but are created automatically at regular intervals when
  enabled for a Droplet.

* [Custom images](https://www.digitalocean.com/docs/images/custom-images/)
  are Linux-based virtual machine images (raw, qcow2, vhdx, vdi, and vmdk
  formats are supported) that you may upload for use on DigitalOcean.

* Distributions are the public Linux distributions that are available to
  be used as a base to create Droplets.

* Applications, or [1-Click Apps](https://www.digitalocean.com/docs/one-clicks/),
  are distributions pre-configured with additional software.

To interact with images, you will generally send requests to the images
endpoint at /v2/images.


# Get Instance

The instance of the `ImagesApi` class can be accessed from the API Client.

```
imagesApi := client.ImagesApi()
```



