# Quail
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
;;;
;;;                                README                                
;;;
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
;;;
;;;
;;;
;;;
;;;  Authors:
;;;     R.W. Oldford 1997 - 2000.
;;;
;;;
;;;----------------------------------------------------------------------------
;;;
;;;
;;;
;;;   This file describes
;;;        A. How to build Quail from code available in the Quail directory system.
;;;        B. Where to find some information on known bugs.
;;;        C. The role of Quail-init.lisp file
;;;
;;;
;;;-----------------------------------------------------------------------------






;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
;;;
;;;
;;;   A. Building Quail from scratch.
;;;
;;;   There are a few steps.
;;;
;;;   1. The Quail directory can be located anywhere provided it's 
;;;      accessible from the Common Lisp application.
;;;      Note: the entire directory structure must remain intact.
;;;
;;;   2. To accommodate the Quail code, and to produce a useful working
;;;      image, the Common Lisp you are working in should have a large
;;;      workspace (e.g. about 20 MB on a Mac PPC).  A substantial fraction
;;;      of this space must be available before building Quail.  On a Mac
;;;      you get this workspace by selecting the MCL (Macintosh Common Lisp)
;;;      icon and then "Get Info" where the required size can be changed.
;;;
;;;   3. Edit the lisp file "quail-make" in the Quail directory.
;;;      There you will need to change some pathnames to suit your local
;;;      system.
;;;
;;;   4. From a fresh Common Lisp image load the lisp file "quail-make".
;;;      You may (or may not ... depending on the CL) be prompted for a few
;;;      answers about the system you are using.
;;;      Quail will begin building itself, informing you of its operations
;;;      as it goes.
;;;
;;;   5. Once the build is finished, in the top-level loop (or listener)
;;;      type
;;;           (in-package :q-user)
;;;           (install-quail-menubar)
;;;
;;;      These will put you in the Quail-user package and install a menu
;;;      driven interface for Quail.
;;; 
;;;   6. Save an image in the appropriate way for your Common Lisp so that
;;;      you can boot Quail directly in the future.
;;;      Type
;;;           (save)
;;;
;;;      You will be prompted for a directory in which to save the Quail
;;;      image (so it had better be writable by the user producing the image!).
;;;      This will produce a Quail image whose default name will be "Quail"
;;;      with appropriate release information attached to the name
;;;      (e.g. "Quail 1.01").
;;;
;;;      Alternatively, you can place it wherever by completely specifying 
;;;      the complete pathname of the desired image file. For example,
;;;
;;;           (save "My Disk:directory1:directory2:Quail")
;;;     
;;;      Now the image will be a file named Quail but located in the
;;;      directory "My Disk:directory1:directory2:". No release information
;;;      will be attached to the file name.
;;;
;;;      
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
;;;
;;;
;;;   B. Known Bugs.
;;;
;;;   In a Quail image execute the form
;;;          (load "q:Comments:whats-new")
;;;
;;;   This will produce a window with mouse selectable buttons.
;;;   If the window is subsequently closed, it can be reproduced by executing
;;;   the form
;;;          (bugs)
;;;   
;;;
;;;      
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
;;;
;;;
;;;
;;;
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
;;;
;;;
;;;   C. The Quail-init file.
;;;
;;;   When the Quail image is booted, it looks for a file called "quail-init" 
;;;   in the *same* directory.  If it finds the file, it will load it.
;;;
;;;   Here is where startup behaviour can be localized by installation.
;;;   (For example, if the Common Lisp operating system interface permits
;;;   identification of the user and their home directory, then Quail-init
;;;   might be edited to load a user-specific init file.)
;;;
;;;   A simple version has been supplied in the topmost Quail directory
;;;   that loads the "whats-new" file mentioned earlier.
;;;   
;;;
;;;      
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;




;;;;;;;;;;;;;;;;;;;;;;;;;;;;;  End of File ;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
