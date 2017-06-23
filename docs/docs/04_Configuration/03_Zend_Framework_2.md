## Using Dephpugger in ZF2

Add in root directory the file `.dephpugger.yml` with the content bellow.

```yml
---
server:
  path: ./public/
  file: index.php
  port: 8080
```

The ZF2 start the server using a command setted in composer.json running `composer serve`.
If you want keep using this command instead of `dephpugger server` and `dephpugger debug`, you can change the composer.json file.

Replace in `scripts` this line.

```json
....
        "serve": "php -S 0.0.0.0:8080 -t public public/index.php",
....
```

To this.

```json
        "serve": "dephpugger server",
```

If you aren't using the dephpugger in global mode, you can run `composer require tacnoman/dephpugger` and add this lines.

```json
        "serve": "php vendor/bin/dephpugger server",
```

And now run in different terminals.

```bash
$ composer serve
$ dephpugger debug # Or php vendor/bin/dephpugger debug
```

Open [http://localhost:8080](http://localhost:8080) and get work!
