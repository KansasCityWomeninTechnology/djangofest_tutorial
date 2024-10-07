# Introduction to the command-line interface

> For readers at home: this chapter is covered in the [Your new friend: Command Line](https://www.youtube.com/watch?v=jvZLWhkzX-8) video.

It's exciting, right?! You'll write your first line of code in just a few minutes! :)

__Let us introduce you to your first new friend: the command line!__

The following steps will show you how to use the black window all hackers use. It might look a bit scary at first but really it's just a prompt waiting for commands from you.

> **Note** Please note that throughout this book we use the terms 'directory' and 'folder' interchangeably but they are one and the same thing.

## What is the command line?

The window, which is usually called the __command line__ or __command-line interface__, is a text-based application for viewing, handling, and manipulating files on your computer. It's much like Windows Explorer or Finder on the Mac, but without the graphical interface. Other names for the command line are: *cmd*, *CLI*, *prompt*, *console* or *terminal*.

## Open the command-line interface

To start some experiments we need to open our command-line interface first.

{% include "/intro_to_command_line/open_instructions.md" %}

## Prompt

You now should see a white or black window that is waiting for your commands.

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}

On Windows, you probably see a `>`, like this:

```
>
```

Take a look at the Linux section -- you'll see something more like that when you get to PythonAnywhere later in the tutorial.

{% endosContent %}

{% osContent "Mac" %}

If you're on Mac, you probably see a `$`, like this:

```
$
```

{% endosContent %}

{% osContent "Linux" %}

If you're on Linux, you probably see a `$`, like this:

```
$
```
    
{% endosContent %}


Each command will be prepended by a `$` or `>` and one space, but you should not type it. Your computer will do it for you. :)

> Just a small note: in your case there may be something like `C:\Users\ola>` or `Olas-MacBook-Air:~ ola$` before the prompt sign, and this is 100% OK.

The part up to and including the `$` or the `>` is called the *command line prompt*, or *prompt* for short. It prompts you to input something there.

In the tutorial, when we want you to type in a command, we will include the `$` or `>`, and occasionally more to the left. Ignore the left part and only type in the command, which starts after the prompt.

## Your first command (YAY!)

> Throughout this workshop, we encourage you to type commands manually into the command line interface (CLI) instead of using copy/paste. It takes longer but, we promise it'll "stick" with you more! :) 

Let's start by typing this command:

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}

```
> whoami
```

{% endosContent %}

{% osContent "Mac" %}

```
$ whoami
```

{% endosContent %}

{% osContent "Linux" %}

```
$ whoami
```

{% endosContent %}

And then hit `enter`. This is our result:

{% filename %}command-line{% endfilename %}
```
$ whoami
olasitarska
```

As you can see, the computer has just printed your username. Neat, huh? :)

> Try to type each command; do not copy-paste. You'll remember more this way!

## Basics

Each operating system has a slightly different set of commands for the command line, so make sure to follow instructions for your operating system.

If you make a typo, you can use the left and right arrow keys to move your cursor, backspace and delete to edit the command. Most command lines don't support using the mouse to move the cursor.

Let's try this, shall we?

### Current directory

It'd be nice to know where are we now, right? Let's see. Type this command and hit `enter`:


<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}

```
> cd
C:\Users\olasitarska
```
> Note: 'cd' stands for 'change directory'. With PowerShell you can use pwd just like on Linux or Mac OS X.

{% endosContent %}

{% osContent "Mac" %}

```
$ pwd
/Users/olasitarska
```

> Note: 'pwd' stands for 'print working directory'.

{% endosContent %}

{% osContent "Linux" %}

```
$ pwd
/Users/olasitarska
```

> Note: 'pwd' stands for 'print working directory'.

{% endosContent %}

You'll probably see something similar on your machine. Once you open the command line you usually start at your user's home directory.

---

### Learn more about a command

Many commands you can type at the command prompt have built-in help that you can display and read! For example, to learn more about the current directory command:

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}

Adding a `/?` suffix to most commands will print the help page. You may need to scroll your command window up to see it all. Try `cd /?`.

{% endosContent %}

{% osContent "Mac" %}

OS X has a `man` command, which gives you help on commands. Try `man pwd` and see what it says, or put `man` before other commands to see their help. The output of `man` is normally paged. Use the space bar to move to the next page, and `q` to quit looking at the help.

{% endosContent %}

{% osContent "Linux" %}

Linux has a `man` command, which gives you help on commands. Try `man pwd` and see what it says, or put `man` before other commands to see their help. The output of `man` is normally paged. Use the space bar to move to the next page, and `q` to quit looking at the help.

{% endosContent %}


### List files and directories

So what's in it? It'd be cool to find out. Let's see:

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}
```
> dir
 Directory of C:\Users\olasitarska
05/08/2020 07:28 PM <DIR>      Applications
05/08/2020 07:28 PM <DIR>      Desktop
05/08/2020 07:28 PM <DIR>      Downloads
05/08/2020 07:28 PM <DIR>      Music
...
```
> Note: In PowerShell you can also use 'ls' like on Linux and Mac OS X.
{% endosContent %}

{% osContent "Mac" %}
```
$ ls
Applications
Desktop
Downloads
Music
...
```
{% endosContent %}

{% osContent "Linux" %}
```
$ ls
Applications
Desktop
Downloads
Music
...
```
{% endosContent %}

---

### Change current directory

Now, let's go to our Desktop directory:

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}
```
> cd Desktop
```
{% endosContent %}

{% osContent "Mac" %}
```
$ cd Desktop
```
{% endosContent %}

{% osContent "Linux" %}
```
$ cd Desktop
```

Note that
the directory name "Desktop" might be translated
to the language of your Linux account.
If that's the case, you'll need to replace `Desktop`
with the translated name;
for example, `Schreibtisch` for German.
{% endosContent %}

Check if it's really changed:

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}
```
> cd
C:\Users\olasitarska\Desktop
```
{% endosContent %}

{% osContent "Mac" %}
```
$ pwd
/Users/olasitarska/Desktop
```
{% endosContent %}

{% osContent "Linux" %}
```
$ pwd
/Users/olasitarska/Desktop
```
{% endosContent %}

Here it is!

> PRO tip: if you type `cd D` and then hit `tab` on your keyboard, the command line will automatically fill in the rest of the name so you can navigate faster. If there is more than one folder starting with "D", hit the `tab` key twice to get a list of options.

---

### Create directory

How about creating a practice directory on your desktop? You can do it this way:

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}
```
> mkdir practice
```
{% endosContent %}

{% osContent "Mac" %}
```
$ mkdir practice
```
{% endosContent %}

{% osContent "Linux" %}
```
$ mkdir practice
```
{% endosContent %}

This little command will create a folder with the name `practice` on your desktop. You can check if it's there by looking on your Desktop or by running a `ls` or `dir` command! Try it. :)

> PRO tip: If you don't want to type the same commands over and over, try pressing the `up arrow` and `down arrow` on your keyboard to cycle through recently used commands.

---

### Exercise!

A small challenge for you: in your newly created `practice` directory, create a directory called `test`. (Use the `cd` and `mkdir` commands.)

#### Solution:

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}
```
> cd practice
> mkdir test
> dir
05/08/2020 07:28 PM <DIR>      test
```
{% endosContent %}

{% osContent "Mac" %}
```
$ cd practice
$ mkdir test
$ ls
test
```
{% endosContent %}

{% osContent "Linux" %}
```
$ cd practice
$ mkdir test
$ ls
test
```
{% endosContent %}

Congrats! :)

---

### Clean up

We don't want to leave a mess, so let's remove everything we did until that point.

First, we need to get back to Desktop:

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}
```
> cd ..
```
{% endosContent %}

{% osContent "Mac" %}
```
$ cd ..
```
{% endosContent %}

{% osContent "Linux" %}
```
$ cd ..
```
{% endosContent %}

Using `..` with the `cd` command will change your current directory to the parent directory (that is, the directory that contains your current directory).

Check where you are:

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}
```
> cd
C:\Users\olasitarska\Desktop
```
{% endosContent %}

{% osContent "Mac" %}
```
$ pwd
/Users/olasitarska/Desktop
```
{% endosContent %}

{% osContent "Linux" %}
```
$ pwd
/Users/olasitarska/Desktop
```
{% endosContent %}

Now time to delete the `practice` directory:

> __Attention__: Deleting files using `del`, `rmdir` or `rm` is irrecoverable, meaning _the deleted files will be gone forever_! So be very careful with this command.

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}
! This will delete your directory !
```
> rm -r practice
```
Windows Command Prompt:
```
> rmdir /S practice
practice, Are you sure <Y/N>? Y
```
{% endosContent %}

{% osContent "Mac" %}
! This will delete your directory !
```
$ rm -r practice
```
{% endosContent %}

{% osContent "Linux" %}
! This will delete your directory !
```
$ rm -r practice
```
{% endosContent %}

Done! To be sure it's actually deleted, let's check it:

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}
```
> dir
```
{% endosContent %}

{% osContent "Mac" %}
```
$ ls
```
{% endosContent %}

{% osContent "Linux" %}
```
$ ls
```
{% endosContent %}

### Exit

That's it for now! You can safely close the command line now. Let's do it the hacker way, alright? :)

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}
```
> exit
```
{% endosContent %}

{% osContent "Mac" %}
```
$ exit
```
{% endosContent %}

{% osContent "Linux" %}
```
$ exit
```
{% endosContent %}

Cool, huh? :)

## Summary

 Here is a summary of some useful commands:

Command (Windows) | Command (Mac OS / Linux) | Description                | Example
----------------- | ------------------------ | -------------------------- | ---------------------------------------------
exit              | exit                     | close the window           | **exit**
cd                | cd                       | change directory           | **cd test**
cd                | pwd                      | show the current directory | **cd** (Windows) or **pwd** (Mac OS / Linux)
dir               | ls                       | list directories/files     | **dir**
copy              | cp                       | copy file                  | **copy c:\test\test.txt c:\windows\test.txt**
move              | mv                       | move file                  | **move c:\test\test.txt c:\windows\test.txt**
mkdir             | mkdir                    | create a new directory     | **mkdir testdirectory**
rmdir (or del)    | rm                       | delete a file              | **del c:\test\test.txt**
rmdir /S          | rm -r                    | delete a directory         | **rm -r testdirectory**
[CMD] /?          | man [CMD]                | get help for a command     | **cd /?** (Windows) or **man cd** (Mac OS / Linux)

These are just a very few of the commands you can run in your command line, but you're not going to use anything more than that today.

If you're curious, [ss64.com](http://ss64.com) contains a complete reference of commands for all operating systems.

## Ready?

Let's dive into Python!
