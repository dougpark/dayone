# dayone
Better Touch Tool create a DayOne journal entry

I created a Better Touch Tool keyboard shortcut to save the highlighted text to a DayOne journal. I use this all the time to save command line tools for later use.

You must have Better Touch Tool installed
You must have DayOne installed
You must have DayOne2 CLI installed

Create a journal in DayOne, my example journal name is "Tech"

Create an All Apps keyboard shortcut in BTT, I used the new Ultra Key feature to map Caps-Lock as a meta key. It's a great way to have a lot of simple keyboard shortcuts. I mapped it to the "a" key, since it was close to the caps lock key and easy to reach.

The first action is to save the selected text to a BTT variable called selected_text.

I then quickly show a BTT HUD (this is optiona) that a "Save to DayOne" command has been issued.

Finally, I issue a terminal command with BTT. This command calls the DayOne2 CLI and passes it the arguments to create the entry.

/usr/local/bin/dayone2 - path and command to execute
-j tells DayOne the name of the journal to use, in this case my "Tech" journal
Tech - name of the journal to use
new - Dayone2 command to run, in this case create a new entry
"{selected_text}" a string of text to place in the new DayOne entry, selected_text is the BTT variable created in the first step, the braces {} tell BTT to substitue the actual text value for the variable name.

That's it. Now when I highlight some text and then his CapsLock A it will create a new DayOne entry.

![BTT Command](https://github.com/dougpark/dayone/blob/main/btt_dayone.png?raw=true)
