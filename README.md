# Install Composer

## Solution 1:

Using CURL for Mac, Linux or Windodw Subsystem Linux ( WSL )
```
# Make sure php already installed
php -version

curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
```

## Solution 2:

### Install Composer on Window with Xampp:

First build path **"c:/xampp/php/"** to execute **php**

Open Command Prompt then go to **"c:/xampp/php/"** directory.

Run this command to install **latest composer**:
```
# Make sure php already installed
php -version

php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('SHA384', 'composer-setup.php') === '669656bab3166a7aff8a7506b8cb2d1c292f042046c5a994c43155c0be6190fa0355160742ab2e1c88d40d5be660b410') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"

echo @php "%~dp0composer.phar" %*>composer.bat
```
### Install Composer on Ubuntu

Open Terminal then paste script below:
```
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('SHA384', 'composer-setup.php') === '669656bab3166a7aff8a7506b8cb2d1c292f042046c5a994c43155c0be6190fa0355160742ab2e1c88d40d5be660b410') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"

mv composer.phar /usr/local/bin/composer
```

Or download from https://getcomposer.org/download/


### Now test by type:
```
composer
```
