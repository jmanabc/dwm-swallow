# dwm-swallow

It's dwm, but only has the swallow patch. This repo was born of frustration.
Basically, the Swallow patch as it is on Suckless.org is completely and fundementally broken in multiple ways. Both the patch command and git apply fail to add functionality, despite successfully adding all the lines of code in the diff. Using https://github.com/LukeSmithxyz/dwm, a version of dwm with functional swallow, I manually edited dwm.c to match in just the spots relevent to swallow. There weren't many huge changes, but Luke's version doesn't use a scanner variable and removed a spot that referenced BSD. This fact may mean that FreeBSD compatibility is broken, but I have no way to check that, so just proceed with caution if you happen to use FreeBSD. Finally, the patch messes up the capitalization when specifying the rules for st in config.h. It should be "St", not "st"; I also set noswallow for st to 0 instead of -1, but I didn't do this step for Firefox's rules, so if this in any way breaks Firefox, that's what you should check first.

I created a .diff that can be found in the releases, if you just want to add this onto your own build.
