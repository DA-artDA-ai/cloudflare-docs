---
pcx_content_type: example
product: Rules
title: Rewrite path of welcome page for visitors in specific countries
---

# Rewrite path of welcome page for visitors in specific countries

To have a welcome page in two languages, create two rewrite URL rules with a static rewrite of the path component:

**Rewrite URL rule #1**

{{<example>}}

Text in **Expression Editor**:

```txt
http.request.uri.path == "/welcome.html" && ip.geoip.country == "GB"
```

Text after **Path** > **Rewrite to...** > _Static_:

```txt
/welcome-gb.html
```

{{</example>}}

**Rewrite URL rule #2**

{{<example>}}

Text in **Expression Editor**:

```txt
http.request.uri.path == "/welcome.html" && ip.geoip.country == "PT"
```

Text after **Path** > **Rewrite to...** > _Static_:

```txt
/welcome-pt.html
```

{{</example>}}
