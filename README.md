# Composer-git ignoring core 


Here i trying to create an environment from a git repository that do not include core folder, and initial set up is manage with composer.

### Process
- Clone repository.
- Run 'composer update' to download dependencies including core.
- Run a normal drupal installation process.
- Run 'drush config-set "system.site" uuid "[uuid]"' uuid is in the resources/uuid.txt file
- Delete all shortcuts Home > Administration > Configuration > User interface > Shortcuts (admin/config/user-interface/shortcut), than in "List links" of "Default" I deleted every shortcut.
- Import the settings Home > Administration > Configuration > Development > Configuration synchronization(import all)
- Untar the dbdump 'tar -zxvf [dbdump.tar.gz]' from resources folder
- import the db 'mysql -h [db-host] -u [user] -p[pass] [db-name] < [dbdump-file].sql'

### Resources
https://github.com/drupal-composer/drupal-project

