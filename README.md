# govCMS (Drupal 8) distribution composer-based installer

## Installation

### Server Requirements

* Apache, Nginx, Microsoft IIS or any other web server with proper PHP support
* Supported PHP Version 7.1.*
* MySQL 5.5.3/MariaDB 5.5.20/Percona Server 5.5.8 or higher with PDO and an InnoDB-compatible primary storage engine
* PostgreSQL 9.1.2 or higher with PDO
* SQLite 3.7.11 or higher

**Dependencies**

* [Git](http://git-scm.com/)
* [Composer](https://getcomposer.org/)

### Installing govCMS

govCMS Drupal 8 utilizes [Composer](https://getcomposer.org/) to manage its dependencies. So, before using govCMS, make sure you have Composer installed on your machine.

For a better composer performance, we recommend

```
composer global require "hirak/prestissimo:^0.3"
```

#### Via Composer Create-Project

```
composer create-project --stability dev --no-interaction govcms/govcms8 MY_PROJECT
```

Composer will create a new directory called MY_PROJECT containing a docroot directory with a full govCMS code base therein.

And you can update govCMS Distribution via (noting that at this stage, updating this way may break some of the dependencies within the distribution, and is generally not recommended unless you know what you're doing!)

```
cd MY_PROJECT
composer update
```

**What are the differences between composer update and composer install?**

* ```composer update``` is mostly used in the *development phase* to upgrade the project packages specified in the composer.json file
* ```composer install``` is primarily used in the *deploying phase* to install the project on a production server or on a testing environment, using the same dependencies stored in the composer.lock file created by composer update

### Troubleshooting

If you're encountering some oddities, [here's a list of resolutions](https://github.com/govCMS/govCMS8-core/wiki/Troubleshooting) to some of the problems you may be experiencing.
