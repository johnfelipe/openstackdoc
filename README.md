
## PHP Calendar Module Installation steps.


Run server with sudo user

```
sudo su
```
Go to main folder 

```
cd /
```

Go to Root folder
```
cd root
```

Move to lnmp/src folder

```
cd lnmp/src
```
Extract php-7.2.5 in /src folder

```
tar -xzf php-7.2.5.tar.gz
```
Move to php-7.2.5/ext/calendar folder 

```
cd php-7.2.5/ext/calendar
```
Check php version detail
```
/usr/local/php/bin/phpize  
```
Make configuration setting to compile calendar extension
```
./configure --with-php-config=/usr/local/php/bin/php-config
```
load calendar extension
```
make && make-install
```
Test build 
```
make test
```
run install command again 
```
make install
```

Important Info:
copy extension path as above result.
For Example (cd /usr/local/php/lib/php/extensions/no-debug-non-zts-20170718/)

Note: Every new image extensions path may be different please make sure copy it from above command result.

Move into extension folder. 
```
cd /usr/local/php/lib/php/extensions/no-debug-non-zts-20170718/
```
Add module to ini file via below command.
```
echo 'extension=calendar.so' > /usr/local/php/etc/php.d/ext-calendar.ini
```
compile php-fpm make compiled version of php
```
sudo service php-fpm restart
```
Final steps
```
Now in your browser you can run this link http://200.122.209.132/phpinfo.php when you search for calendar using Ctrl+f you will find your calendar extension easily or you can find through command line using command “php -i” it will show you same information as it showing in browser
```












