# symfony-intl-infinite-loop-fixer
Provider a small fix for Symfony 2.7|2.8 with locale composee from PHP Intl extension.

1. Add the GitHub repos to composer repositories
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

2. Install the package
```bash
composer require messi89/symfony-intl-infinite-loop-fixer
```

3. Exclude symfony original locale file from autoload
```json
{
    "autoload": {
        "exclude-from-classmap": [
             "vendor/symfony/symfony/src/Symfony/Component/Intl/Locale.php"
        ]
    }
}
```

4. Now you can enable php intl again
```bash
phpdenmod -v 7.2 intl 
service php7.2-fpm restart
```

5. Enjoy !
