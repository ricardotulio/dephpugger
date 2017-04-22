Dephpugger is a tool to debug codes for PHP application in development.

## Why?
In another languages (like Python and Ruby), is really normal start a web server in terminal and start to develop you application code. In PHP many people install the nginx or apache to make run an application in local development. But, after PHP 5.4, you can start your webserver running a simple command too.

```bash
$ php -S localhost:8080
```

I prefer this mode, because you don't need install many things, only PHP.
Following another languages example, if you are a Python developer and you want start a debug in a breakpoint to check the code flow, you can use the lib Ipdb, and in the same server you will see the code stopping and in terminal will appear the code lines.

In ruby language is very similar, you can install the lib Byebug and start use. You need only write `byebug` in your code and you have the same effect described in Python language.

But, if you are a PHP developer, you must install xDebug first, choose an IDE or editor, search for a tutorial `how integrate <my editor> with xDebug`. If you want change the IDE, you must install again. This is really bad, because many developers can't install and prefer to use `var_dump($variable); die()` to see a variable value in each request.

This project is the solution for this problems, you will start a built-in web server in one terminal and the debugger in another terminal. Is really easy to use.
