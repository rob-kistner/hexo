---
title: Eloquent Collections
date: 2020-04-25 10:38
categories:
- Laravel
tags:
- PHP
- Laravel
- Eloquent
- Collections
- Relationships
---

## Relationships

`hasMany` and `belongsTo` relationship tables can pull each other's records. Given Task and Projects tables, this will pull the first Task's parent project:

```php
Task::first()->project
```

#### Pulls values as an array

```php
Category::all()
  ->pluck(['category']);
```

#### Pulls out a single value as a string

```php
Category::all()
  ->where('id', 1)
  ->pluck(['category'])
  ->first();
```