# UBUNTU - Tested in 16.04 and most in 18.04
This is a simple/short guide to execute common commands when using PHP, Apache in an Ubuntu Server

## Identify the current user and it's groups

> Command `id`

> Output `uid=1002(cfv) gid=1002(cfv) groups=1002(cfv),27(sudo)`

## List directory files and privileges
> Command `ls -la`

> Example `ls -la /var/www`

## Change owner of folder use `-R` to make it recursive to internal folders
> Command `sudo chown -R $USER:$USER /var/www/html`

> Example `sudo chown username: myfolder`

> Example `sudo chown -R $USER:www-data storage`

> Example `sudo chown -R $USER:www-data bootstrap/cache`

## Change permisions of folder use `-R` to make it recursive to internal folders 
> Command `chmod -R 775`

> Example `chmod -R 775 storage`

> Example `chmod -R 775 bootstrap/cache`

The number in the permissions depends on what level of access you want to give to your users.

## Edit `.bashrc` file
> Command `sudo vim .bashrc`

Usually you can add custom commands to your terminal here, above you will find some use cases.

## Alias to create shortcuts to directory inside `.bashrc` file
> Command `alias cdo='cd /var/www/html/'`

> `cdo` will be the command you tipe in console after adding the alias.

## Alias to set username and email of Git automatically 
> Command `alias gitUE="git config user.email 'my@email.com'; git config user.name 'My Git Name'"`

This is useful too to remember how to set them up in a fresh dev environment.

## disable or/and enable phpmyadmin
> Command `alias phpmyadminDisable="sudo a2disconf phpmyadmin.conf; sudo service apache2 restart"`

> Command `alias phpmyadminEnable="sudo a2enconf phpmyadmin.conf; sudo service apache2 restart"`

# Contributions and corrections
If you want to contribute or correct some of the content in this list please feel free to do it in an always friendly and free way.
