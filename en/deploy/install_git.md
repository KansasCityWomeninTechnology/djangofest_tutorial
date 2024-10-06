Git is a "version control system" used by a lot of programmers. This software can track changes to files over time so that you can recall specific versions later. A bit like the "track changes" feature in word processor programs (e.g., Microsoft Word or LibreOffice Writer), but much more powerful.

## Installing Git

<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}

You can download Git from [git-scm.com](https://git-scm.com/). You can hit "next" on all steps except for two: in the step where it asks to choose your editor, you should pick Nano, and in the step entitled "Adjusting your PATH environment", choose "Use Git and optional Unix tools from the Windows Command Prompt" (the bottom option). Other than that, the defaults are fine. Checkout Windows-style, commit Unix-style line endings is good.

Do not forget to restart the command prompt or PowerShell after the installation finished successfully.
    
{% endosContent %}

{% osContent "Mac" %}

Download Git from [git-scm.com](https://git-scm.com/) and follow the instructions.

> **Note** If you are running OS X 10.6, 10.7, or 10.8, you will need to install the version of git from here: [Git installer for OS X Snow Leopard](https://sourceforge.net/projects/git-osx-installer/files/git-2.3.5-intel-universal-snow-leopard.dmg/download)

{% endosContent %}

{% osContent "Linux" %}

#### Installing Git: Debian or Ubuntu

```bash
$ sudo apt install git
```

#### Installing Git: Fedora

```bash
$ sudo dnf install git
```

#### Installing Git: openSUSE

```bash
$ sudo zypper install git
```
 
{% endosContent %}
