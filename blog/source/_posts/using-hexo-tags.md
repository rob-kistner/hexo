---
title: Using Hexo Tags
date: 2020-04-25 10:23:53
tags:
- Tags
- YouTube
- Quotes
---

Ways to include media, etc. in your posts.

See https://hexo.io/docs/tag-plugins for a full list.

### YouTube

Using the `YouTube` tag.

```ejs
{% youtube GDP9LQWMlMU %}
```

gives you this result...

{% youtube GDP9LQWMlMU %}

***

### Quote

Using the `blockquote` tag.

```ejs
{% blockquote %}
Every interaction is both previous and an opportunity…
{% endblockquote %}
```

yields this...

{% blockquote Author Name https://nothing.com %}
Every interaction is both previous and an opportunity…
{% endblockquote %}

***

### Codeblock

Pretty much works just like making a code callout in markdown…

{% codeblock lang:html %}
<html>
<head>
  <title>This is a page</title>
</head>
<body>
{% endcodeblock %}

***

### Raw HTML

By using the `raw` tag, you can include straight html in your post…

```ejs
{% raw %}
<strong style="color: red">Example of Strong with style</strong>
{% endraw %}
```

yields...

{% raw %}
<strong style="color: red">Example of Strong with style</strong>
{% endraw %}

***