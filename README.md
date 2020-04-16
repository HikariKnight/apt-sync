# apt-sync
an extension for apt and apt-get to emulate what "pacman -Syu" does on arch

Arch and arch based systems have been able to run pacman -Syu to update the repositories and then upgrade packages on their system.
Me as a debian user always wondered why this was never baked into apt or apt-get, so i wrote my own "module" to achieve that.

The installation is very easy. Make the apt script executable with ```chmod +x apt``` then you just copy the script "apt" to /usr/local/bin/ and you will now be able to run "sudo apt sync" to update your repositories and upgrade your packages in one command, you can also pass -y after sync to automatically accept the changes.

If you use apt-get instead of apt then you can rename the script to apt-get and copy it to /usr/local/bin/ and it will work identically to what i described above except you use apt-get instead of apt.
You can also copy the script and symlink it as apt-get to /usr/local/bin/apt-get too, that also works.
