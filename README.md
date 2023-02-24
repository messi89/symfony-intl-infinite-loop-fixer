# symfony-intl-infinite-loop-fixer
Provider a small fix for Symfony 2.7|2.8 with locale compose from PHP Intl extension.

- Add the GitHub repos to composer repositories
```json
{
    "repositories": [
        {
            "url": "https://github.com/messi89/symfony-intl-infinite-loop-fixer",
            "type": "git"
        }
    ]
}
```

- Install the package
```bash
composer require messi89/symfony-intl-infinite-loop-fixer
```

- Exclude symfony original locale file from autoload
```json
{
    "autoload": {
        "exclude-from-classmap": [
             "vendor/symfony/symfony/src/Symfony/Component/Intl/Locale.php"
        ]
    }
}
```

- Now you can enable php intl again
```bash
phpenmod -v 7.2 intl 
service php7.2-fpm restart
```
### Enjoy !
