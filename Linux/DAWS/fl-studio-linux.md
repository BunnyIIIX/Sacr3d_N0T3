# FL-Studio-Linux


### FL Studio 12 Download.

* Download: [FL_Studio-12](https://mega.nz/file/7nBgxL6S#Y2WVpdziVWII49cUy8VTUN_eDnYqUCoPjo9-3bRbfiA)
* Password: 123


### How To Install FL STUDIO 12 on LINUX! (WITHOUT BUGS)

1. Download playonlinux.
```bash
    sudo apt install playonlinux
```
2. Run `playonlinux` and make sure it launches.

3. Go to Tools -> Manage Wine Versions.
   In Wine versions (x86), install the version 1.9.15.
   Select the version in the left box and click ")".

4. Click Install and then Install a non-listed program.

5. Click through the welcome screen.

6. Select "Install a program in a new virtual drive".

7. Pick a name for your virtual drive (like "flstudio").

8. In the next window, don't check anything and click Next.

9. Select "32-bit Windows installation". Then wait a minute while
   your drive is being created.

10. Next click Browse and look for your FL Studio installation
    .exe. One thing to note is that your main file system in Wine
    is always mapped under the disk letter Z:.

11. Click through the installation. Once you reach the "Choose
    which features of FL Studio 12 you want to install", uncheck
    Desktop icons and Asio4All. Install everything in its default
    directories.

12. In the final screen, select "FL" as your shortcut.

13. Once FL Studio is installed, try to run it and make sure it
    launches. You will most likely not see any text and the
    program will not be registered.

14. To fix the no text issue, select the FL in your playonlinux
    main window, go to Configure -) Install components and
    install the Microsoft Core Fonts and tahoma packages.

15. To register your copy of FL Studio, go to Configure -) Wine
    -) Registry Editor. Then go to Registry -) Import Registry
    File... and navigate to where your registration key is
    located. Then exit the registry editor.

16. Launch your FL Studio and verify that everything works (for
    instance, open newstuff.flp).

17. Open audio settings and set your sound driver to FL Studio
    ASIO.


