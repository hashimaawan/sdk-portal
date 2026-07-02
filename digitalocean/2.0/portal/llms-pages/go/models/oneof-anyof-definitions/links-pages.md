# Links Pages

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkxpbmtzUGFnZXM


# Class Name

`LinksPages`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`models.Pages`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/pages.md) | models.LinksPagesContainer.FromPages(models.Pages pages) |
| [`models.Pages1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/pages-1.md) | models.LinksPagesContainer.FromPages1(models.Pages1 pages1) |
| [`interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | models.LinksPagesContainer.FromObject(interface{} object) |


# models.Pages

## Initialization Code

### Example

```go
value := models.LinksPagesContainer.FromPages(models.Pages{
    Last:                  models.ToPointer("https://api.digitalocean.com/v2/images?page=2"),
    Next:                  models.ToPointer("https://api.digitalocean.com/v2/images?page=2"),
})
```


# models.Pages1

## Initialization Code

### Example

```go
value := models.LinksPagesContainer.FromPages1(models.Pages1{
    First:                 models.ToPointer("https://api.digitalocean.com/v2/images?page=1"),
    Prev:                  models.ToPointer("https://api.digitalocean.com/v2/images?page=1"),
})
```


# interface{}

## Initialization Code

### Example

```go
value := models.LinksPagesContainer.FromObject(interface{}("[key1, val1][key2, val2]"))
```



