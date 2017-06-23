## Configuring in your project

The dephpugger use default values to run. For example, the server run in a port `8888`. But there is a way to change theese configurations.
The Dephpugger get the default value, and after this, check if exists a file called `.dephpugger.yml` in root project folder.
If this file exists, the values will be replaced for the default configuration.

The defualt configuration is...

```php
    /**
     * Default config that will be replaced by *.dephpugger.yml* file
     */
    private $defaultConfig = [
        'server' => [
            'port' => 8888,
            'host' => 'localhost',
            'phpPath' => 'php',
            'path' => null,
            'file' => '',
        ],
        'debugger' => [
            'port' => 9005,
            'host' => 'localhost',
            'lineOffset' => 6,
            'verboseMode' => false,
            'historyFile' => '.dephpugger_history',
        ],
    ];
```

Now, you can change the default values creating the file `.dephpugger.yml`.

```yml
--- 
debugger: 
  host: mysocket.dev # default: localhost
  port: 9002 # default: 9005
  lineOffset: 10 # default: 6
  path: ./public/ # default: null
  file: index.php # default: null
  verboseMode: false # default: false
  historyFile: ~/.dephpugger_history # default: .dephpugger_history
server:
  host: myproject.dev # default: localhost
  phpPath: /usr/local/bin/php # default: php
  port: 8080 # default: 8888
```

Ps: You don't need rewrite every configurations, if you want edit only the port for server, you can create this file.

```yml
--- 
server:
  port: 8080
```

All default configurations will keep the default value and the port now is `8080` instead of `8888`.<br>
Now, restart the dephpugger and be happy ;D.
