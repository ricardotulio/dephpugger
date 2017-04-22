**Daux.io** is an documentation generator that uses a simple folder structure and Markdown files to create custom documentation on the fly. It helps you create great looking documentation in a developer friendly way.

[TOC]

## Features

### For Authors


### For Developers


### For Marketing


## Demos

This is a list of sites using Daux.io:

## Getting Started

### Install

```
composer global require justinwalsh/daux.io
```

You can then use the `daux` command line to generate your documentation.

If the command isn't found, ensure your `$PATH` contains `~/.composer/vendor/bin`

### Writing pages

Creating new pages is very easy:
1. Create a markdown file (`*.md` or `*.markdown`)
2. Start writing

By default, the generator will look for folders in the `docs` folder.
Add your folders inside the `docs` folder. This project contains some example folders and files to get you started.

You can nest folders any number of levels to get the exact structure you want.
The folder structure will be converted to the nested navigation.

You must use underscores instead of spaces. Here are some example file names and what they will be converted to:

**Good:**

* 01_Getting_Started.md = Getting Started
* API_Calls.md = API Calls
* 200_Something_Else-Cool.md = Something Else-Cool
* _5_Ways_to_Be_Happy.md = 5 Ways To Be Happy

**Bad:**

* File Name With Space.md = FAIL

### See your pages

Now you can see your pages. you have two options for that : serve them directly, or generate to various formats.

We recommend the first one while you write your documentation, you get a much quicker feedback while writing.

#### Serving files

You can use PHP's embedded web server by running the following command in the root of your documentation

```
./serve
```

Upload your files to an apache / nginx server and see your documentation


#### Export to other formats

Daux.io is extendable and comes by default with three export formats:

- Export to HTML, same as the website, but can be hosted without PHP.
- Export all documentation in a single HTML page
- Upload to your Atlassian Confluence server.


To export, run the `daux` command and your documentation will be generated in `static` (you can change the destination with the `--destination` option)


## Configuration


## PHP Requirements

Daux.io is compatible with PHP 5.5 and up.

The reason is because some dependencies we have (mainly Symfony and Guzzle) do not support php 5.4 anymore.

### Extensions

PHP Needs the following extension to work : `php-mbstring` and `php-xml`.

If you encounter an error similar to `utf8_decode() not found` this means that you're missing the `php-xml` package. (We've seen it happen only on PHP 7)

## Known Issues

- __Windows UTF-8 files support__ Files with UTF-8 characters cannot be handled on windows with PHP5, PHP7 should work fine.


## Support

If you need help using Daux.io, or have found a bug, please create an issue on the <a href="https://github.com/justinwalsh/daux.io/issues" target="_blank">GitHub repo</a>.
