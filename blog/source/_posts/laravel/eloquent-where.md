---
title: Eloquent Where
date: 2020-04-25 10:39
categories:
- Laravel
tags:
- PHP
- Laravel
- Eloquent
- Where
---

### Fetch records matching `where` clause

```php
Gear::where('category', '=', 'Lenses')->get();
```

or just eliminate the `=`:

```php
Gear::where('category', 'Lenses')->get();
```

### Fetch single record

```php
Project::where('id', 3)->get();
```

### Fetch first record

```php
Project::where('quan', 3)->first();
```

### Find in JSON field

Below, in the Cast Model, there's a JSON column called `titles` where we're trying to find `Director`.

```php
Cast::whereJsonContains('titles', 'Director')->get();
```