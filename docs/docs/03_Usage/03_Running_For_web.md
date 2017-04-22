## Running for web

Forget your apache, forget your nginx in your local development. The PHP has a built in web server in php-cli since 5.4.0 version. You can start a webserver running this simple command.

```bash
$ php -S localhost:8000
```

If you open in your browser http://localhost:8000, you will se working. The Symfony framework has a command to start a webserver too `php bin/console server:start`.
Now, you will use the dephpugger's web server. The Dephpugger webserver will use the this command, but with more parameters to connect with dephpugger's debug.

To start a web server application, run.

```bash
$ dephpugger server
```

<img src="/images/dephpugger-server.png">

This commands run `php -S <host>:<port> -t /path/to/project -dxdebug.remote_enable=1 -dxdeb...` this command in background.

Create a simple `index.php` with a simple hello world and see working.
You can change the default port changing the [configuration](04_Configuration).

Open another terminal window and start the dephpugger.

```bash
$ dephpugger debug
```

In your index.php code, add this line.

```php
xdebug_break();
```

You must activate your browser plugin (How activate my brower plugin? Click [here](02_Installation/04_Browser_Plugin.md))

Now you can refresh the page and see the debugger works.

See an example using Lumen framwork.
In this example, exist a bug because the $_GET return always a string and the code need an integer.
Solving this in video bellow.

<img src="https://raw.githubusercontent.com/tacnoman/dephpugger/master/images/dephpugger-web.gif">
