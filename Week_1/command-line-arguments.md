# Command line arguments

## What are Command Line Arguments?

Command line arguments are strings of text used to pass additional information to a program when an application is run through the command line interface (CLI) of an operating system. Command line arguments typically include information used to set configuration or property values for an application.

In most cases the arguments are passed after the program name in your prompt. An example of the syntax of command line arguments looks like this:

```
$ [runtime] [script_name] [argument-1 argument-2 argument-3 ... argument-n]
```

Here runtime can be anything that executes a program/script e.g. sh, java, node, etc. The arguments are usually separated by a space - however there are some runtimes that use commas to distinguish between multiple command line arguments. Also, depending on the program, you can pass arguments in the form of key-value pairs, which we'll see later in this article.

## Why use CLA

Why Use Command Line Arguments?
The following are some of the major benefits of using command line arguments:

- You can pass information to an application before it starts. This is particularly useful if you want to perform large number configuration settings.
- Command line arguments are passed as strings to your program. String data types can easily be converted to other data types within an application, making the arguments very flexible.
- You can pass unlimited number of arguments via the command line.
  Command line arguments are used in conjunction with scripts and batch files, which is particularly useful for automated testing.
