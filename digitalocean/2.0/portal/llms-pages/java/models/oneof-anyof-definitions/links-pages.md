# Links Pages

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkxpbmtzUGFnZXM


# Class Name

`LinksPages`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`Pages`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/pages.md) | LinksPages.fromPages(Pages pages) |
| [`Pages1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/pages-1.md) | LinksPages.fromPages1(Pages1 pages1) |
| `Object` | LinksPages.fromObject(Object object) |


# Pages

## Initialization Code

### Example

```java
LinksPages.fromPages(
        new Pages.Builder()
            .last("https://api.digitalocean.com/v2/images?page=2")
            .next("https://api.digitalocean.com/v2/images?page=2")
            .build()
    )
```


# Pages1

## Initialization Code

### Example

```java
LinksPages.fromPages1(
        new Pages1.Builder()
            .first("https://api.digitalocean.com/v2/images?page=1")
            .prev("https://api.digitalocean.com/v2/images?page=1")
            .build()
    )
```


# Object

## Initialization Code

### Example

```java
LinksPages.fromObject(
        ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}")
    )
```



