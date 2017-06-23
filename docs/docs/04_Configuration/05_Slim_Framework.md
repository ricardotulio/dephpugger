## Using Dephpugger in Slim Framework

Add in root directory the file `.dephpugger.yml` with the content bellow.

```yml
---
server:
  path: ./public/
  port: 8080

```

Run the commands bellow in different terminal windows (You must run in the root path).

```bash
$ dephpugger server
$ dephpugger debug
```

Open [http://localhost:8080](http://localhost:8080) and get work!
