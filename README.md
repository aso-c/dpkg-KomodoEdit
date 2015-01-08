dpkg-KomodoEdit
===============

"Debianisation" the Komodo Edit installation tarball:
  create Debian package for Komodo Edit from it's tarball

Homepage: http://komodoide.com/komodo-edit/
Source code: https://github.com/Komodo/KomodoEdit
Origin: http://komodoide.com/download/edit-linux
(x86-64: http://komodoide.com/download/edit-linux64)


##Building debian package

1. Create package directory with name by scheme:
    [package_name]-[version]-[debian-revision]
2. Checkout/clone Debian control directory in this calalog.
3. Create symlink into original Komodo Edit tarball with name komoidoiedit-<version>-<debian_revision>.
4. Fix the content debian/rules, debian/control & debian/changelog files with actual information
    about version, architecture & current maintainer of debianising Komodo Edit tarball.
4. Run debuild --no-lintian -b
    Additional options:
        -us - not subscribe source
        -uc - not subscribe changelog
        -ai386 - force set architecture to i386 (not work) 
        -ai386 - force set architecture to i386 (on amd64 cross-compile) 

