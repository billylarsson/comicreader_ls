Comicreader LS
======

Important
-----
This software isn't publicly announced, if you’re here reading this you most likely got a link from me at Discord or something, meaning that its early-alpha. Its still messy, buggy and crashy you should take mature precautions before pointing this program to your valuable collection!

Reading features 
-----
***Mode1:*** Single page one per turn is resized and shown to fit the screen while maintaining aspect ratio.

***Mode2:*** Same as mode1 but with two pages per turn (if one image is very wide, mode1 is used for the current page and mode2 will be turned back on once two images can fit the same screen together)

***Mode3:*** Single page that’s resized to fit the screens width where you can scroll up and down with the mouse.
If you press ‘P’ a minipage-widget will be shown to the right where you see all the pages from the loaded comic, you can click anywhere inside to go directly to that page. Pressing ‘P’ again disables the minipage-widget.

***Bookmarking:***
Right clicking a page and you’ll have the option to set a bookmark with a comment, also while right clicking if there are any bookmarks already such will be available and while clicking one takes you directly to that page.


Comicvine features
-----
If you rightclick on a cover and there's a API key present in the settings an option will be shown: Comicvine Widget.
The software tries to figure out what comic you just feed into the widget and if there are any suggestions they will be shown and recommended for you.
Also far down the bottom more comics will be show that matches adjacent comics-files on your computer, you can map several comics at once this way.
You can freely search publishers and once clicking on them they should be added to your local cache, same applies for volumes and issues.
You should see in the list of issues which comics you have in your collection as bolded text and missing/yet unmapped comics as thinner text.
If a comic isn't in your drive there's a sign "TOKEN ONLY".
Once a comic is properly linked you can click the link to get straight to the comicvine page regarding that comic.
Outside the Comicvine widget, if a comic is properly linked, while clicking on it you should see its volume location to the left, and clicking on this left list takes you to that comic, if you click a comic you dont have, a token is shown. 

Dangerous Indexing feature
-----
***THIS ONLY TARGETS COMICVINE ID LINKED ISSUES!***

To enable you should enter the database manually and put a path to any folder that you want to copy your comic files into while sorting them.
This will result in the old file being renamed to *.backup and the new file will be properly sorted for you.

ie, say you have this comic: "/Downloads/comics/Weekly_Pack2020.10.21/Batman and Robin #23.cbz" and it is properly linked with corresponding Comicvine ID.
It will be copied to "/Your desired location/DC Comics/Batman and Robin #17827/Batman and Robin #23.cbz" where #17827 is the unique volume ID for that volume. 
initializing dangerous indexing can only be done from the command line: python launcher.py dangerous
This feature shouldn't be used unless you really know what you're doing and realizing the danger it include, that's why its not accessible from the GUI.

WEBP converter
-----
This is the least tested feature, it works properly under Linux.
It converts your comics to WEBP (or JPEG) re-compresses them and REPLACES the old file, same as Dangerous Indexing... you shouldn't use this feature unless you know what you're doing!

Installation
-----
Grab a zipfile either Windows or Linux, unpack into the directory of your choice. 

Not sure how a Mac users should do but compiling the source files Mac OS should work (I don’t have a Mac, therefore I haven't tried)


Preparation
-----
You need to have Python installed: `https://www.python.org/downloads/`

Running: pip install -r requirements.txt –user may install everything needed.
If you’re having trouble with WEBP, causing the program to crash you should:

`pip install webp –user`

If you’re still experiencing crashes due to WEBP a fix can be to (especially for Anaconda users):

`pip install –upgrade pillow –user`

If you’re on Windows, there may be problems if you don't have WinRAR installed.


Windows users
-----
Windows have a few complications with long paths and filenames from within compressed archives, therefore there can be crashes if you’re asking to handle such files.
A temporary solution to this can be if you’re mapping/mounting/choosing directories that aren't that lengthy such as C:\TMP for cache and C:\Comics for your library.
Also, subprocesses are used for Windows and its not adequately tested if that’s sustainable. 



Run
-----
You run the program from you command line: `python launcher.py` (..perhaps `python3 laucher.py` etc…)
You could use the full path of a CBR/CBZ file as an argument and if should get you right into the page one of that comic.
`Python3.8 launcher.py “C:\Comics\Super Hero\Wearing a pyjamas 001.cbz”`
