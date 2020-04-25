---
title: Using Hexo Assets
date: 2020-04-25 10:25:00
tags:
- Hexo
- Images
---

### Including Imags

Including like this...

```md
![Image 1](/images/image1.png)
```

![Image 1](/images/image1.png)

You can also use an ejs `img` tag like so, including option width, height, and alt text…

```md
{% img "/images/image2.png" 300 150 "Alt Text" %}
```

{% img "/images/image2.png" 300 150 "Alt Text" %}