---
title: Eloquent Find
date: 2020-04-25 10:38
categories:
- Laravel
tags:
- PHP
- Laravel
- Eloquent
- Collections
- Find
---

## Find by id and show relationship records with `hasMany`

```php
Film::find(3)->cast;
```