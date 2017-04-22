## About Dephpugger

Now, you have installed the Dephpugger in your machine. You can run this command to see if all is ok.
For the next tutorials we will use the command `dephpugger` global. If you are using local, you can change the command `dephpugger` to `php vendor/bin/dephpugger`.

```bash
$ dephpugger requirements
```

You will see this.

<img src="/images/dephpugger-requirements.png">

## Running Dephpugger

To run a webserver debug or a cli application debug, you must start two windows in terminal. In the first to start a webserver built-in or cli and in the second, the debugger.

Open a terminal and run this command:

```bash
$ dephpugger debug
```

You will see this.

<img src="/images/dephpugger-debug.png">

The debugger start a socket server in port 9005 and now is waiting a breakpoint.
Now, create a simple php file to test.

```php
<?php

# File test.php

$int = 1;
$array = ['one', 'two', 'three'];

echo $int;
echo $array[1];
```

Now, add a command `xdebug_break();` in your code. Like this.

```php
<?php

# File test.php

$int = 1;
$array = ['one', 'two', 'three'];

xdebug_break(); # <-- Add this line

echo $int;
echo $array[1];
```

Open another terminal, and run.

```bash
$ debugger cli test.php
```

The breakpoint is created, and you can see the debugger start.

<img src="/images/dephpugger-breakpoint.png">
