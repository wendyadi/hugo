---
title: title
# linktitle:
description: Converts all characters in the provided string to title case.
godocref:
date: 2017-02-01
publishdate: 2017-02-01
lastmod: 2017-02-01
categories: [functions,fundamentals]
menu:
  docs:
    parent: "functions"
#tags: [strings]
signature: ["title INPUT"]
workson: []
hugoversion:
relatedfuncs: []
deprecated: false
aliases: []
---


```
{{title "BatMan"}}` → "Batman"
```

Can be combined in pipes. In the following snippet, the link text is cleaned up using `humanize` to remove dashes and `title` to convert the value of `$name` to Intial Caps.

```
{{ range $name, $items := .Site.Taxonomies.categories }}
    <li><a href="{{ printf "%s/%s" "categories" ($name | urlize | lower) | absURL }}">{{ $name | humanize | title }} ({{ len $items }})</a></li>
{{ end }}
```