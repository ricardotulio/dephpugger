## Commands

When the debugger stop in a breakpoint, it wait the developer send commands to navigate in code.

Create a file called `quicksort.php` (or with another algorithm). We will use this file for example.

```php
<?php
$unsorted = array(43,21,2,1,9,24,2,99,23,8,7,114,92,5);

function quick_sort($array)
{
	$length = count($array);
	if($length <= 1){
		return $array;
	} else {
		$pivot = $array[0];
		$left = $right = array();
		for($i = 1; $i < count($array); $i++)
		{
			if($array[$i] < $pivot){
				$left[] = $array[$i];
			} else {
				$right[] = $array[$i];
			}
		}
		return array_merge(quick_sort($left), array($pivot), quick_sort($right));
	}
}

xdebug_break();

$sorted = quick_sort($unsorted);

echo 'Unsorted numbers: ',implode(', ', $unsorted).PHP_EOL;
echo 'Sorted numbers: '.implode(', ', $sorted).PHP_EOL;
```

Run in different terminals.

```bash
$ dephpugger debug # in first terminal
$ dephpugger cli quicksort.php # in another terminal
```

<img src="/images/dephpugger-quicksort-breakpoint.png">

The debugger is waiting you to run a command. If you run the command help, you will see all possible commands.

| Command           | Alias | Explanation                                                          |
|-------------------|-------|----------------------------------------------------------------------|
| next              | n     | To run a step over in code                                           |
| step              | s     | To run a step into in code                                           |
| continue          | c     | To continue script until found another breakpoint or finish the code |
| list              | l     | Show next lines in script                                            |
| list-previous     | lp    | Show previous lines in script                                        |
| help              | h     | Show help instructions                                               |
| $variable         |       | Get a value from a variable                                          |
| $variable = 33    |       | Set a variable                                                       |
| my_function()     |       | Call a function                                                      |
| dbgp(< command >) |       | To run a command in dbgp                                             |
| quit              | q     | Exit the debugger                                                    |

Now you can navigate in the algorithm and investigate.

Press `n` to go to the next line, if exists.<br>
Press `s` and press enter to get inside the method.<br>
Press `l` to see the next lines.<br>
Press `lp` to see the previous lines.<br>
Key the variable name to get the value and type.<br>
You can change the variable value in runtime.<br>

## See example

<script type="text/javascript" src="https://asciinema.org/a/115976.js" id="asciicast-115976" async></script>
