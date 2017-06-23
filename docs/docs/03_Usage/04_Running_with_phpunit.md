## Running with PHPUNIT (or another test suit)

The dephpugger running cli, only create a complex command and run in terminal. To use PHPUNIT isn't different. Follow the steps bellow.

### Install phpunit

First, you can install in multiple different ways. The most simple is installing using the composer.<br>
Run the code bellow in your root project path.

```bash
$ composer require "phpunit/phpunit":"*"
```

This command will install the phpunit executable in path `vendor/bin/phpunit`.<br>
Now, instead of run the code `vendor/bin/phpunit` to run the tests, you must run:

```bash
$ dephpugger cli vendor/bin/phpunit
```


Ps: If you install in global path, you can run using only `dephpugger cli phpunit`, or if you prefer use the `phar` file `dephpugger cli /path/to/phpunit.phar`.<br>
Ps2: If you install the phpunit using Homebrew (Mac OS X) this command doesn't work, because the executable file using Homebrew is a bash script calling a phar file, not a php file.

## Using with another test tool

You can use in the same way for different suit tests. For example, if you want use with codeception, follow these steps.

```bash
# Install first
$ composer install "codeception/codeception":"*"

# Run tests
$ dephpugger cli vendor/bin/codeception
```

To run behat or another, you must only change the codeception's path to another.

## Adding parameteres to test suit

If you are want pass parameters to your suit test (in example, PHPUNIT), you must add the command between quotation marks.

```bash
$ dephpugger cli "phpunit --bootstrap src/Email.php tests/emailTest"
```

Following example basic example in phpunit documentation, you will see.

<img src="/images/dephpugger-unit-xdebug.png" alt="phpunit with dephpugger + xdebug" />
