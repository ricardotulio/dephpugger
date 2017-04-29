## Using Dephpugger in Silex Framework

Add in root directory the file `.dephpugger.yml` with the content bellow.

```yml
---
server:
  path: ./web/
  port: 8888
```

The Silex Framework start the web application in development using the composer running `composer run`.
Go to your `composer.json` file and replace this:

```json
    "scripts": {
        "run": [
            "echo 'Started web server on http://localhost:8888'",
            "php -S localhost:8888 -t web"
        ]
    }
```

To this:
```json
    "scripts": {
        "run": [
            "echo 'Started web server on http://localhost:8888'",
            "dephpugger server" << This line
        ]
    }
```

If you aren't using the dephpugger in global mode, you can change the line `dephpugger server` to `php vendor/bin/dephpugger server`.

Run the commands bellow in different terminal windows (You must run in the root path).

```bash
$ COMPOSER_PROCESS_TIMEOUT=0 composer run # To start a server
$ dephpugger debug # Or "php vendor/bin/dephpugger debug" in local mode
```

Open [http://localhost:8888](http://localhost:8888) and get work!
