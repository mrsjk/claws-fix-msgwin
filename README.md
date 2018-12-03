# claws-fix-msgwin
claws fix to always open msg in new window

patchfile:
always-open-msg-in-new-window

for those who prefer reading messages in a separate window, not panned
within main window.
it really permanently disables panned msg view within main window,
forces new msg window for every action including ENTER and SPACE keypresses,
menuitem 'view / show or hide / message view', and even ^ button next to
summary in std layout

should be really configurable for pressing ENTER and SPACE keys,
but i really do not need nor like default panned view and like it better
this way.

patchfile:
msgwin_key_jk

that's a small addition to always use j,k keys for message scrolling
within message window, regardless of key accell defs. that allows using
natural srcolling via j and k keys in message window, while having the
same keys defined as accells in main window for other actions (like
srolling summaryview messages list, that was really my intention
to allow natural same scrolling everywhere).
and for right-hand usage there's also hardcoded backslash key for closing
message window (as i usually prefer q for both-hands usage, but also need
near-right-hand no-other-purpose key for right-hand minimal-motion usage
while having a cup of coffee (or whatever) in my left hand).
hardcoding keys is not very elegant of course, but it works, and as my
personal patch it's definitely less invasive than window-context based
menu accell keys (if that's even possible, and if it was, would generate
new and bigger set of problems)


for debian derived distros just put patch file in debian/patches,
add in debian/patches/series and that's it, just run dpkg-buildpackage
or whatever you like.
for other distros find your distro's preferred way or alter source directly
(included patch is more than trivial)

initial version applies to claws-mail-3.14.1 (other versions untested)


as a background, that default behavior of claws-mail prevented me from using it
for a very long time, then i got bored of using evolution (and leaking tons
of memory in a long run), so i did this to become happy claws-mail user.
hopefully this can help other wanna-be claws users, who hate panned msg views, and otherwise can see how cool claws-mail is.


