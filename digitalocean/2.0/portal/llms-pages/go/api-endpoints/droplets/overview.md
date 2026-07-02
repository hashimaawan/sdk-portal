# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkRyb3BsZXRzJTJGT3ZlcnZpZXc

A [Droplet](https://www.digitalocean.com/docs/droplets/) is a DigitalOcean
virtual machine. By sending requests to the Droplet endpoint, you can
list, create, or delete Droplets.

Some of the attributes will have an object value. The `region` and `image`
objects will all contain the standard attributes of their associated
types. Find more information about each of these objects in their
respective sections.


# Get Instance

The instance of the `DropletsApi` class can be accessed from the API Client.

```
dropletsApi := client.DropletsApi()
```



