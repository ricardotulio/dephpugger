## Using Dephpugger in Yii2 Framework

Add in root directory the file `.dephpugger.yml` with the content bellow.

### Basic application
```yml
---
server:
  path: ./web/
  port: 8080
```

Run the commands bellow in different terminal windows (You must run in the root path).

```bash
$ dephpugger server # Instead of php yii serve
$ dephpugger debug
```

### Advanced application

Create a file called `dephpugger.yml` in `frontend/web/` and `backend/web/`.
```yml
---
server:
  port: 8080
```

Go to web folder and run in different terminals.

```bash
$ dephpugger server # Instead of php yii serve
$ dephpugger debug
```

Open [http://localhost:8080](http://localhost:8080) and get work!
