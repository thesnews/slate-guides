---
title: SNworks Developer Docs for Guides

toc_footers:
  - <a href="http://getsnworks.com">Main Site</a>
  - <a href="http://thesnews.github.io/slate/">Gryphon Dev Docs</a>
  - <a href='http://confluence.getsnworks.com/display/ID/Internal+Documentation+Home'>SNworks Internal Docs</a>
  - <a href="http://confluence.getsnworks.com">Client Support Docs</a>
  - <a href="http://uptime.getsnworks.com/">System Status</a>
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

```html
# Code will show up over here.
<a href="#">foo</a>
```

SNworks Developer Docs for *Guides*. If you're looking for Gryphon docs, <a href="http://thesnews.github.io/slate/">look here</a>

<aside class="notice">This only contains docs that **differ** from Gryphon.</aside>


#  Technologies we use

This information is on our <a href="http://confluence.getsnworks.com/display/ID/Documentation+Index">private help section</a>.


# Bitbucket and Git
## Overview

```shell
# Code sample here
```

```html
<a href="#">foo</a>
```

## Helpful Commands

```shell
user> git checkout
```
checkout something

# Dev Web Server

More information on this in our <a href="#">private help docs</a>.

# Twig Extensions and Tips

Overview

## Fetch Tag

## Helper Tag

> Load the config helper, and grab a value

```html
{% helper config %}
{{ config.get('foo.bar') }}
```

> Load the config helper, but call it 'Configuration'

```html
{% helper config as Configuration %}
{{ Configuration.get('foo.bar') }}
```

The helper tag loads Gryphon specific Twig helpers.

Parameter | Description
--------- | -----------
as STRING | Provide an alternate name for the helper (OPTIONAL)

## Config Helper

```html
{% helper config %}

Welcome to <a href="{{config.get('publication.url)}}">{{config.get('publication.name')}}</a>
```

The config helper provides read access to the global configuration system. **This helper has only one method: `get`.**

Common, but not all, config options used in templates:

Config key | Description
---------- | -----------
publication.name | Yeah...
publication.url | The canonical URL for the publication
mail.admin | The default admin email address
gryphon.media.meta | An array of meta properties
gryphon.default.section | The section that constructs the front page
gryphon.comments.disqus_shortname | The site's Disqus shortname

## Request Helper

# Coding for Guides

Creating templates for Guides is fairly simple once you have the basics down.

## base.tpl

<!-- # Authentication

> To authorize, use this code:

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import 'kittn'

api = Kittn.authorize('meowmeowmeow')
```

```code
# With code, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace `meowmeowmeow` with your personal API key.
</aside>

# Kittens

## Get All Kittens

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import 'kittn'

api = Kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```code
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Isis",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import 'kittn'

api = Kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```code
curl "http://example.com/api/kittens/3"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Isis",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">If you're not using an administrator API key, note that some kittens will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the cat to retrieve -->

