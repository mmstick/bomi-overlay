# Installation Instructions
To add this overlay to Gentoo you will first need to install layman and add this github repository's **layman.xml** file to **/etc/layman/layman.cfg**. The contents of that file shall look something like this:

    overlays  : http://www.gentoo.org/proj/en/overlays/repositories.xml
                http://github.com/mmstick/bomi-overlay/raw/master/layman.xml

Following that, you will be able to fetch an updated list of repositories and add the bomi repository.

    sudo layman -f
    sudo layman -a bomi

If this is your first time compiling a Qt application on your Gentoo system, you will need to make a symbolic link to enable the use of qmake for Qt5.

    sudo ln -s /etc/xdg/qtchooser/qt5.conf /etc/xdg/qtchooser/default.conf

Once done, you can simply start the process of adding bomi to your system.

    sudo emerge -av bomi
