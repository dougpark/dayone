# DayOne CLI
Better Touch Tool create a DayOne journal entry

I created a Better Touch Tool keyboard shortcut to save the highlighted text to a DayOne journal. I use this all the time to save text snippets for later use. I like how DayOne automatically adds the current date and time to the entry.

* You must have [Better Touch Tool](https://folivora.ai/downloads) installed
* You must have [DayOne](https://dayoneapp.com) installed
* You must have [DayOne2 CLI](https://help.dayoneapp.com/en/articles/435871-command-line-interface-cli) installed

Create a journal in DayOne, my example journal name is "Tech"

Create an All Apps keyboard shortcut in BTT, I used the new [Hyper Key](https://www.macsparky.com/blog/2021/2/hyper-key-via-bettertouchtool) feature to map caps-lock as a meta key. It's a great way to have a lot of simple keyboard shortcuts. I mapped it to the "A" key, since it was close to the caps-lock key and easy to reach.

1. The first action is to save the selected text to a BTT variable called selected_text.

2. I then quickly show a BTT HUD (this is optional) that a "Save to DayOne" command has been issued.

3. Finally, I issue a terminal command with BTT. This command calls the DayOne2 CLI and passes it the arguments to create the entry.

* /usr/local/bin/dayone2 - path and command to execute
* -j tells DayOne the name of the journal to use, in this case my "Tech" journal
* Tech - name of the journal to use
* new - Dayone2 command to run, in this case create a new entry
* "{selected_text}" a string of text to place in the new DayOne entry, selected_text is the BTT variable created in the first step, the braces {} tell BTT to substitue the actual text value for the variable name.

That's it. Now when I highlight some text and press caps-lock A it will create a new DayOne entry.

![BTT Command](https://github.com/dougpark/dayone/blob/main/btt_dayone.png?raw=true)
