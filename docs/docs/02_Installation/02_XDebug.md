## Installation of XDebug

Follow this steps.

### For Linux

First, run this command:

```bash
$ sudo apt-get install php-xdebug
```

### For Mac Os X

```bash
$ brew install php-xdebug
```

### For Windows users

I'm sorry :/
You can use Docker or Vagrant or make a pull request for me :D

Activating the xDebug
-------

Now you have the xDebug installed in your machine.
After this, you must change the file php.ini to your php-cli and active this one.

To see if your xDebug is installed, you can run.

```bash
$ php -i | grep "xdebug support" --color
xdebug support => enabled
```

If the result bring `disabled`, you must change your php.ini file or your `xdebug.ini` file (if exists).
First, try to get the `xdebug.ini file`.

```bash
$ php -i | grep xdebug.ini
/etc/php/7.0/cli/conf.d/20-xdebug.ini
```

If doesn't exist, you can get the php.ini file, you can run.

```bash
$ php -i | grep php.ini --color

Configuration File (php.ini) Path => /etc/php/7.0/cli
Loaded Configuration File => /etc/php/7.0/cli/php.ini
```

Open your the `.ini` file with your editor (must sudo user) and add this line.

```ini
zend_extension=/path/to/your/xdebug.so
```

Run again and check if your xdebug is installed.

```bash
$ php -i | grep "xdebug support" --color
xdebug support => enabled
```

You can get more info about installation <a href="https://xdebug.org/docs/install" target="_blank">clicking here</a>.
