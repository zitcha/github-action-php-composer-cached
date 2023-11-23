
> :warning: **This is a *public* repository** :warning:

Custom Github Actions must be in a public repository (Except when using Github Enterprise which allows private repositories)

### Github Action - PHP Composer Cached

Simple Example:

```
    steps:
      - name: Composer install with Cache
        uses: the-pistol/github-action-php-composer-cached@master
        with:
          composer-working-dir: .
```

Dev-only using a differnt path:

```
    steps:
      - name: Composer install with Cache
        uses: the-pistol/github-action-php-composer-cached@master
        with:
          composer-working-dir: ./my-app  # Directly which contains composer.lock and composer.json
          dev: yes  # install dev-only packages
```