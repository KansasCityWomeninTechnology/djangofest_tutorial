<button class="osToggle" data-os="Windows">Windows</button>
<button class="osToggle" data-os="Mac">Mac</button>
<button class="osToggle" data-os="Linux">Linux</button>

{% osContent "Windows" %}

Depending on your version of Windows and your keyboard, one of the following should open a command window (you may have to experiment a bit, but you don't have to try all of these suggestions):
- Go to the Start menu or screen, and enter "Command Prompt" in the search field.
- Go to Start menu → Windows System → Command Prompt.
- Go to Start menu → All Programs → Accessories → Command Prompt.
- Go to the Start screen, hover your mouse in the lower-left corner of the screen, and click the down arrow that appears (on a touch screen, instead flick up from the bottom of the screen). The Apps page should open. Click on Command Prompt in the Windows System section.
- Hold the special Windows key on your keyboard and press the "X" key. Choose "Command Prompt" from the pop-up menu.
- Hold the Windows key and press the "R" key to get a "Run" window. Type "cmd" in the box, and click the OK key.

![Type "cmd" in the "Run" window](../python_installation/images/windows-plus-r.png)

Later in this tutorial, you will need to have two command windows open at the same time. However, on some versions of Windows, if you already have one command window open and you try to open a second one using the same method, it will instead point you to the command window you already have open. Try it now on your computer and see what happens! If you only get one command window, try one of the other methods in the list above. At least one of them should result in a new command window being opened.

{% endosContent %}

{% osContent "Mac" %}

Go to Applications → Utilities → Terminal.

{% endosContent %}
{% osContent "Linux" %}

It's probably under Applications → Accessories → Terminal, or Applications → System → Terminal, but that may depend on your system. If it's not there, you can try to Google it. :)

{% endosContent %}
