# Subscription Tier Slug

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlN1YnNjcmlwdGlvblRpZXJTbHVn

The slug of the subscription tier to sign up for. Valid values can be retrieved using the options endpoint.


# Enum Type Name

`SubscriptionTierSlug`


# Fields

| Name |
|  --- |
| `STARTER` |
| `BASIC` |
| `PROFESSIONAL` |


# Example

```python
from digitaloceanapi.models.subscription_tier_slug import SubscriptionTierSlug

subscription_tier_slug = SubscriptionTierSlug.STARTER
```



