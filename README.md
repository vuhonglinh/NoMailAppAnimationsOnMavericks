No Mail.app Animations on OS X 10.9 Mavericks
=============================================

A Mailbundle plugin to disable the Mail.app Send- and Reply-animations on OS X 10.9 Mavericks. Run on your own risk. When having issues, please remove the 
Mailbundle again.


How does it work?
================
This Plugin disables Mail.app animations in 10.9 by swizzling Mail.app's -[DocumentEditor shouldDoPopOutAnimation] to return NO always.
To disable the send-animation, we swizzle -[DocumentEditor _performSendAnimation] to directly call -[DocumentEditor __sendAnimationCompleted]


How to Install Automatically?
=============================

1) Disable GateKeeper (System Preferences > Security & Privacy > General tab > Allow apps downloaded from: Anywhere

2) Download https://github.com/AndreasVerhoeven/NoMailAppAnimationsOnMavericks/releases/download/mail7-2/DisableMailAnimationsForMavericks.pkg
and run the Installer.

How to Install Manually?
========================
1) Copy AveNoAnimationsInMailPlugin.mailbundle  to ~/Library/Mail/Bundles/

2) run 'defaults write com.apple.mail EnableBundles -int 1' in Terminal.app (without the quotes, of course)

3) Restart Mail.app

