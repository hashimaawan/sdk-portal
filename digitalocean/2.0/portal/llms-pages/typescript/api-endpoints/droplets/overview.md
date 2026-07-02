# Overview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0aCUyRl9fYXBpX3JlZmVyZW5jZSUyRkRyb3BsZXRzJTJGT3ZlcnZpZXc

A [Droplet](https://www.digitalocean.com/docs/droplets/) is a DigitalOcean
virtual machine. By sending requests to the Droplet endpoint, you can
list, create, or delete Droplets.

Some of the attributes will have an object value. The `region` and `image`
objects will all contain the standard attributes of their associated
types. Find more information about each of these objects in their
respective sections.


# Create Instance

The instance of the `DropletsApi` class can be created using the API Client.

```
const dropletsApi = new DropletsApi(client);
```



