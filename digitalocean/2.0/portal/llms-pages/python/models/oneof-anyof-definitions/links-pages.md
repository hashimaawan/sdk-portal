# Links Pages

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkxpbmtzUGFnZXM


# Data Type

`Pages | Pages1 | Any`


# Cases

| Type |
|  --- |
| [`Pages`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/pages.md) |
| [`Pages1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/pages-1.md) |
| [`Any`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) |


# Pages

## Initialization Code

### Example

```python
value = Pages(
    last='https://api.digitalocean.com/v2/images?page=2',
    next='https://api.digitalocean.com/v2/images?page=2'
)
```


# Pages1

## Initialization Code

### Example

```python
value = Pages1(
    first='https://api.digitalocean.com/v2/images?page=1',
    prev='https://api.digitalocean.com/v2/images?page=1'
)
```


# Any

## Initialization Code

### Example

```python
value = jsonpickle.decode('{"key1":"val1","key2":"val2"}')
```



