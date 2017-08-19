https://github.com/cfenollosa/bashblog is a wonderful script for producing a static blog, but it has some quirks.

I found out that it doesn't keep track of any changes made when in "edit full html" mode, so I wrote this script to keep my fancier blog pages from being clobbered.

If you're writing locally and posting to the web and you have SSH or SFTP access, the "cp" commands can be replaced by "scp" or "rsync" or other software that moves content between networked computers.

This script may seem weird at first reading, but after you've messed around with bashblog a bit, it should make sense.

I am not very technically literate, but this works for me.

Hopefully it can help you.
