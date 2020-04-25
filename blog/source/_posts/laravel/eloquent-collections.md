---
title: Eloquent Collections
date: 2020-04-25 10:36
categories:
- Laravel
tags:
- PHP
- Laravel
- Eloquent
- Collections
---

## Collection functions

Diff'ing will remove records from an `all()` find after the fact. Below, all records are retrieved, then any category matching 'Anvil Knives' is removed.

```php
$categories = Category::all();
$categories = $categories->diff(
  Category::where(
    'category', '=', 'Anvil Knives'
  )->get()
);
```

### Reject certain values

An easy way to reject primary key values from an existing collection. Below, items with primary keys with values 2 & 3 are removed.

```php
$categories = Category::all();
$categories = $categories->except([2, 3]);
```

### Return a list of primary keys for items in a collection

```php
$categories = Category::all();
$idList = $categories->modelKeys();
```

### Hide values in a collection

```php
$categories = Category::all();
$categories->makeHidden(['created_at', 'updated_at']);
```

They're just hidden though, you could show them again with

```php
$categories->makeVisible(['created_at', 'updated_at']);
```

## Find a record or create it

If you want to see if a record exists already, and create it if it doesn't, you can use `firstOrCreate`.

```php
$user = User::firstOrCreate(['email' => $email]);
```