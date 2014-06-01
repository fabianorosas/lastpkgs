lastpkgs
=========

Lists and removes packages installed during the last sessions. Good for moments of package-installing frenzy.

Sometimes when experimenting with new programs or doing things in a rush the filesystem is left with a lot of junk installed. This small script aims to help in these situations by fetching the packages that were installed in the current session and removing them upon user approval.

+ `# lastpkgs -r`

prompts for deletion of the recently installed packages
+ `$ lastpkgs -l 3`

lists packages installed explicitly in the last 3 sessions.
+ `$ lastpkgs -a 50`

lists all packages installed in the last 50 sessions (including the ones that came in as dependencies).
