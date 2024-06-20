
> :warning: **This is a *public* repository** :warning:

Custom Github Actions must be in a public repository (Except when using Github Enterprise which allows private repositories)

### Github Action - PHP Composer Cached

Example 1 - Include Dev Packages:

```
    steps:
      - name: Composer install with Cache
        uses: the-pistol/github-action-php-composer-cached@v1.0.0
        with:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          composer-working-dir: .
          dev-option: "include-dev"
```

Example 2 - Exclude Dev packages and use alternative path:

```
    steps:
      - name: Composer install with Cache
        uses: the-pistol/github-action-php-composer-cached@v1.0.0
        with:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          composer-working-dir: ./my-app  # Directly which contains composer.lock and composer.json
          dev-option: "exclude-dev"
```