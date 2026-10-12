Laravel Eloquent Query Cache
============================

![CI](https://github.com/renoki-co/laravel-eloquent-query-cache/workflows/CI/badge.svg?branch=master)
[![codecov](https://codecov.io/gh/renoki-co/laravel-eloquent-query-cache/branch/master/graph/badge.svg)](https://codecov.io/gh/renoki-co/laravel-eloquent-query-cache/branch/master)
[![StyleCI](https://github.styleci.io/repos/223236785/shield?branch=master)](https://github.styleci.io/repos/223236785)
[![Latest Stable Version](https://poser.pugx.org/rennokki/laravel-eloquent-query-cache/v/stable)](https://packagist.org/packages/rennokki/laravel-eloquent-query-cache)
[![Total Downloads](https://poser.pugx.org/rennokki/laravel-eloquent-query-cache/downloads)](https://packagist.org/packages/rennokki/laravel-eloquent-query-cache)
[![Monthly Downloads](https://poser.pugx.org/rennokki/laravel-eloquent-query-cache/d/monthly)](https://packagist.org/packages/rennokki/laravel-eloquent-query-cache)
[![License](https://poser.pugx.org/rennokki/laravel-eloquent-query-cache/license)](https://packagist.org/packages/rennokki/laravel-eloquent-query-cache)

Laravel Eloquent Query Cache brings back the `remember()` functionality that has been removed from Laravel a long time ago.
It adds caching functionalities directly on the Eloquent level, making use of cache within your database queries.

## Fork notice

This is a Calq fork of [renoki-co/laravel-eloquent-query-cache](https://github.com/renoki-co/laravel-eloquent-query-cache),
maintained to keep the package working on Laravel 13. Changes against upstream `3.6.1`:

- `src/Traits/QueryCacheable.php` registers the flush observer without instantiating the model, because Laravel 13
  throws when `observe()` is called while the model is still booting.
- `composer.json` supports `illuminate/database` and `illuminate/support` `^12.0|^13.0`. Laravel 10 and 11 are
  dropped: every one of their releases is blocked by a Composer security advisory, so they can no longer be
  installed or tested without disabling advisory checks.
- The test suite runs on Laravel 12 and 13, Livewire 4 and PHPUnit 13.

## 🤝 Supporting

**If you are using one or more Renoki Co. open-source packages in your production apps, in presentation demos, hobby projects, school projects or so, sponsor our work with [Github Sponsors](https://github.com/sponsors/rennokki). 📦**

[<img src="https://github-content.s3.fr-par.scw.cloud/static/37.jpg" height="210" width="418" />](https://github-content.renoki.org/github-repo/37)

## 📃 Documentation

[The entire documentation is available on Gitbook 🌍](https://rennokki.gitbook.io/laravel-eloquent-query-cache/)

## 🐛 Testing

``` bash
vendor/bin/phpunit
```

## 🤝 Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## 🔒  Security

If you discover any security related issues, please email alex@renoki.org instead of using the issue tracker.

## 🎉 Credits

- [Alex Renoki](https://github.com/rennokki)
- [All Contributors](../../contributors)
