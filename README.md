##README

Provaider que integra o SFTP ao strorage do laravel 5.*

##Composer Instalação

composer require jailtonsc/sftp-laravel

##Integração com o Laravel

No arquivo config/app.php em providers insira no provaider

SFTP\SFTPServiceProvider::class

E no arquivo config/filesystems.php insira 

```php
'sftp' => [
	'driver'   => 'sftp',
	'host' => 'example.com',
	'port' => 21,
	'username' => 'username',
	'password' => 'password',
	'privateKey' => 'path/to/or/contents/of/privatekey',
	'root' => '/path/to/root',
	'timeout' => 10,
],
```

Munde o 

```php
'default' => 'sftp'
```