## Dephugger

You can install dephpugger in two different ways.
In your local project or in global path.

```bash
# Global mode
$ composer global require "tacnoman/dephpugger":"dev-master"

# Local mode
$ composer require "tacnoman/dephpugger":"dev-master"
```

## For global mode
When you use composer in global mode, it creates a folder called `.composer` in your home.
Open your `~/.bash_profile` and add this lines.

```bash

if [ -d "$HOME/.composer/vendor/bin" ] ; then
  PATH="$PATH:$HOME/.config/composer/vendor/bin"
fi

```

Now you can run the command `dephpugger`.

## For local mode

```bash
php vendor/bin/dephpugger
```

You will see this:

<img src="/images/dephpugger-command.png">
