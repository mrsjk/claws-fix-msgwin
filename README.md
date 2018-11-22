# claws-fix-msgwin
claws fix to always open msg in new window

for those who prefer reading window in a separate window, not panned within main window.
it really permanently disables panned msg view within main window,
forces new msg window for every action including <enter>, <space>,
menuitem 'view / show or hide / message view', and even button next to summary in std layout

should be really configurable for actions like <enter> <space> but i really do not need nor like
default panned view and like it better this way.

for debian derivated distros just put patch file in debian/patches, add in debian/patches/series
and that's it, just run dpkg-buildpackage or whatever you like.
for other distros find your way or alter source directly (included patch is more than trivial)

initial version applies to claws-mail-3.14.1 (other versions untested)


as a background, that default behavior of claws-mail holded me from using it for a very long time,
then i got bored of using evolution (and leaking tons of memory in a long run), so i did this to become
happy claws-mail user
