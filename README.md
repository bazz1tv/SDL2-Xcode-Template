SDL2 Xcode4 Templates
======================

Tah-Dah


Pre-Requisites
---------------
Designed to work with the SDL2.framework in your /Library/Frameworks folder.
If you need to look in another directory for your frameworks, please just add to SDL2 Base.xctemplate/TemplateInfo.plist @ the bottom, near <key>LIBRARY_SEARCH_PATHS</key> :) You'll figure it out :) 

Install
---------------
To install the Templates, simply copy the Project Templates folder into ~/Library/Developer/Xcode/Templates

Notes
-------
There are 2 different Templates, one for SDL2 Console application, and one for SDL2 Regular Application. 

The difference is that one is simply a command line app.
the other is an actual .app file (with the .app bundle hierarchy and all).

Technical Notes
---------------
Since I compiled my SDL2 without X11 support, I'm not sure what happens when you have X11 support in your SDL2 framework.
Maybe you can let me know :) 

All I do is compile with -framework SDL2 -framework cocoa for this template and it works fine, I'm just not sure if it's because I installed SDL2 without X11 support. Let me know :) if it works for you :) 
Also, you may wonder why am i templating with linker flags instead of adding the frameworks directly/visually into the XCode template/project??
  -- Because I could not find a way for the template file to locate the SDL2.framework in /Library/frameworks folder. There were 2 workarounds
     -- a) Use the other linker flags and do -framework SDL2 -framework cocoa <- i did this
     -- b) add SDL2.framwork into /System/Library/Frameworks directory (which is a hunch),  because the Cocoa framework loaded fine.


--
Havefun! If you have any questions... Hit me up!!!

My email is mbazzinotti __ AT __ gmail.com


