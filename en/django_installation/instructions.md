> Part of this section is based on tutorials by Geek Girls Carrots (https://github.com/ggcarrots/django-carrots).

> Part of this section is based on the [django-marcador
tutorial](http://django-marcador.keimlink.de/) licensed under the Creative Commons
Attribution-ShareAlike 4.0 International License. The django-marcador tutorial
is copyrighted by Markus Zapke-Gründemann et al.


## Virtual environment

Before we install Django we will get you to install an extremely useful tool to help keep your coding environment tidy on your computer. It's possible to skip this step, but it's highly recommended. Starting with the best possible setup will save you a lot of trouble in the future!

So, let's create a **virtual environment** (also called a *virtualenv*). Virtualenv will isolate your Python/Django setup on a per-project basis. This means that any changes you make to one website won't affect any others you're also developing. Neat, right?

All you need to do is find a directory in which you want to create the `virtualenv`; your home directory, for example. On Windows, it might look like `C:\Users\Name\` (where `Name` is the name of your login).

> __NOTE:__ On Windows, make sure that this directory does not contain accented or special characters; if your username contains accented characters, use a different directory, for example, `C:\djangofest`.

For this tutorial we will be using a new directory `djangofest` from your home directory:

{% filename %}command-line{% endfilename %}
```
$ mkdir djangofest
$ cd djangofest
```

We will make a virtualenv called `myvenv`. The general command will be in the format:

{% filename %}command-line{% endfilename %}
```
$ python3 -m venv myvenv
```

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}

To create a new `virtualenv`, you need to open the command prompt and run `python -m venv myvenv`. It will look like this:

```
C:\Users\Name\djangofest> python -m venv myvenv
```

Where `myvenv` is the name of your `virtualenv`. You can use any other name, but stick to lowercase and use no spaces, accents or special characters. It is also a good idea to keep the name short – you'll be referencing it a lot!

{% endosContent %}

{% osContent "Mac" %}

We can create a `virtualenv` on OS X by running `python3 -m venv myvenv`.
It will look like this:

```
$ python3 -m venv myvenv
```

`myvenv` is the name of your `virtualenv`. You can use any other name, but stick to lowercase and use no spaces. It is also a good idea to keep the name short as you'll be referencing it a lot!

__NOTE:__ If you get an error like

>```
>E: Unable to locate package python3-venv
>```

then instead run:
>```
>sudo apt install python{{ book.py_version }}-venv
>```

{% endosContent %}

{% osContent "Linux" %}

We can create a `virtualenv` on Linux by running `python3 -m venv myvenv`.
It will look like this:

```
$ python3 -m venv myvenv
```

`myvenv` is the name of your `virtualenv`. You can use any other name, but stick to lowercase and use no spaces. It is also a good idea to keep the name short as you'll be referencing it a lot!

__NOTE:__ On some versions of Debian/Ubuntu you may receive the following error:

>```
>The virtual environment was not created successfully because ensurepip is not available.  On Debian/Ubuntu systems, you need to install the python3-venv package using the following command.
>    apt install python3-venv
>You may need to use sudo with that command.  After installing the python3-venv package, recreate your virtual environment.
>```
In this case, follow the instructions above and install the `python3-venv` package:
>```
>$ sudo apt install python3-venv
>```

__NOTE:__ On some versions of Debian/Ubuntu initiating the virtual environment like this currently gives the following error:

>```
>Error: Command '['/home/eddie/Slask/tmp/venv/bin/python3', '-Im', 'ensurepip', '--upgrade', '--default-pip']' returned non-zero exit status 1
>```

To get around this, use the `virtualenv` command instead.

>```
>$ sudo apt install python-virtualenv
>$ virtualenv --python=python{{ book.py_version }} myvenv
>```

> __NOTE:__ If you get an error like

>```
>E: Unable to locate package python3-venv
>```

then instead run:
>```
>sudo apt install python{{ book.py_version }}-venv
>```

{% endosContent %}

## Working with virtualenv

The command above will create a directory called `myvenv` (or whatever name you chose) that contains our virtual environment (basically a bunch of directories and files).

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}

Start your virtual environment by running:

```
C:\Users\Name\djangofest> myvenv\Scripts\activate
```

__NOTE:__ On Windows 10 you might get an error in the Windows PowerShell that says `execution of scripts is disabled on this system`. In this case, please ask a mentor to help you resolve the issue.

<!-- (This comment separates the two blockquote blocks, so that GitBook and Crowdin don't merge them into a single block.) -->

__NOTE:__ For users of the popular editor VS Code, which comes with an integrated terminal based off windows PowerShell, if you wish to stick with the integrated terminal, you may run the following command to activate your virtual environment:
>
>```
>$ . myvenv\Scripts\activate.ps1
>```
>The advantage is that you don't have to switch between editor windows and command-line windows

{% endosContent %}

{% osContent "Mac" %}

Start your virtual environment by running:

```
$ source myvenv/bin/activate
```

Remember to replace `myvenv` with your chosen `virtualenv` name!

__NOTE:__ If the command `source` is not available, try doing this instead:
>```
>$ . myvenv/bin/activate
>```

{% endosContent %}

{% osContent "Linux" %}

Start your virtual environment by running:

```
$ source myvenv/bin/activate
```

Remember to replace `myvenv` with your chosen `virtualenv` name!

__NOTE:__ If the command `source` is not available, try doing this instead:
>```
>$ . myvenv/bin/activate
>```

{% endosContent %}

You will know that you have `virtualenv` started when you see that the prompt in your console is prefixed with `(myvenv)`.

When working within a virtual environment, `python` will automatically refer to the correct version so you can use `python` instead of `python3`.

OK, we have all important dependencies in place. We can finally install Django!

## Installing Django {#django}

Now that you have your `virtualenv` started, you can install Django.

Before we do that, we should make sure we have the latest version of `pip`, the software that we use to install Django:

{% filename %}command-line{% endfilename %}
```
(myvenv) ~$ python -m pip install --upgrade pip
```

### Installing packages with requirements

A requirements file keeps a list of dependencies to be installed using
`pip install`:

First create a `requirements.txt` file inside of the `djangofest/` folder, using the code editor that you installed earlier. You do this by opening a new file in the code editor and then saving it as `requirements.txt` in the `djangofest/` folder. Your directory will look like this:

```
djangofest
├── myvenv
│   └── ...
└───requirements.txt
```

In your `djangofest/requirements.txt` file you should add the following text:

{% filename %}djangofest/requirements.txt{% endfilename %}
```
Django~={{ book.django_version }}
```

Now, run `pip install -r requirements.txt` to install Django.

{% filename %}command-line{% endfilename %}
```
(myvenv) ~$ pip install -r requirements.txt
```
{% filename %}What you'll see{% endfilename %}
```
Collecting Django~={{ book.django_version }} (from -r requirements.txt (line 1))
  Downloading Django-{{ book.django_version }}-py3-none-any.whl (7.9MB)
Installing collected packages: Django
Successfully installed Django-{{ book.django_version }}
```

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}

If you get an error when calling pip on Windows, please check if your project pathname contains spaces, accents or special characters (for example, `C:\Users\User Name\djangofest`). If it does, please consider using another place without spaces, accents or special characters (suggestion: `C:\djangofest`). Create a new virtualenv in the new directory, then delete the old one and try the above command again. (Moving the virtualenv directory won't work since virtualenv uses absolute paths.)

Your command line might freeze when you try to install Django. If this happens, instead of the above command use:

```
C:\Users\Name\djangofest> python -m pip install -r requirements.txt
```

{% endosContent %}

{% osContent "Linux" %}

If you get an error when calling pip on Ubuntu 12.04 please run:
``` 
`python -m pip install -U --force-reinstall pip` 
```
to fix the pip installation in the virtualenv.

{% endosContent %}

That's it! You're now (finally) ready to create a Django application!
