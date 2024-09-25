Add this recipe to a site by running the following commands.

### Tell composer where the recipe lives.
```
composer config repositories.az-digital/pantheon-imagemagick-configuration vcs "git@github.com:az-digital/pantheon-imagemagick-configuration"
```
### Require the recipe via composer.
```
composer require az-digital/pantheon-imagemagick-configuration
```
_Note: Drush 13 and later required to apply recipes via drush._
Example command to upgrade: 
```
composer require "drush/drush:13.2.0 as 12.4.3"  
```

### Apply the recipe to your site via drush.
```
lando drush recipe ../recipes/pantheon-imagemagick-configuration
```


To do everything that this recipe does without the recipe, use `drush config:set`
```
drush en -y imagemagick
drush config:set imagemagick.settings:quality 92
drush config:set imagemagick.settings:prepend '-limit memory 64MiB'
```
