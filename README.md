![GitHub downloads](https://img.shields.io/github/downloads/jonelo/jacksum-fbi-linux/total?color=green)

# Jacksum File Browser Integration on GNU/Linux

The installer script installs [Jacksum](https://github.com/jonelo/jacksum) and [HashGarten](https://github.com/jonelo/HashGarten) which allow accessing Jacksum's primary features from the GNU/Linux file browser/file manager's script menu.

## System Requirements

- A GNU/Linux or Unix operating system

- A graphical desktop user interface

- bash v3 or later, or zsh

- At least one of the supported file browsers below

- A Java Runtime Environment (JRE) or Java Developement Kit (JDK) with graphical libraries, version 11 or later. Note: a headless OpenJDK is not suitable to run the HashGarten GUI. 

- jacksum-3.7.0.jar, HashGarten-0.14.0.jar and flatlaf-2.3.jar (all jars are part of the installation tarball)

### Supported File Browsers

The installation script has been tested successfully for many file browsers on many systems. See also the head of the installer script for details.

| File Browser           | Tested Versions | API                  | Comment                                                                                                     |
|------------------------|-----------------|----------------------|-------------------------------------------------------------------------------------------------------------|
| [Caja](https://github.com/mate-desktop/caja)          | 1.12.0 - 1.26.0 | Caja                 | It is the default file manager for the MATE desktop environment. It is a fork of Nautilus version 2.32.     |
| [Dolphin](https://apps.kde.org/de/dolphin/)           | 2.2 - 21.12.3   | KDE                  | Default file manager on KDE-powered distributions.                                                          |
| [elementary files](https://github.com/elementary/files) | 6.2.1         | elementary contracts | "elementary files" is the file manager used by the elementary OS.                                         |
| [Konqueror](https://apps.kde.org/de/konqueror/)       | 3.4.1 - 4.4.2   | KDE                  | Konqueror was the file manager for KDE before it was replaced by Dolphin starting with KDE 4.               |
| [Krusader](https://krusader.org/)                     | 2.7.2           | KDE                  | Krusader is a file manager for KDE.                                                                         |
| [Nemo](https://github.com/linuxmint/nemo)             | 1.8.4 - 5.2.4   | Nemo                 | Nemo is Linux Mint's default file manager in Cinnamon desktop edition. It is a fork of Nautilus 3.4.        |
| [GNOME Files (Nautilus)](https://gitlab.gnome.org/GNOME/nautilus) | 2.6.1 - 24.6    | GNOME                | Default file manager for GNOME-powered distributions like Fedora and Ubuntu.                    |
| [ROX-Filer](https://github.com/rox-desktop/rox-filer) | 2.5 - 2.24.33   | ROX                  | ROX-Filer is the file manager for the desktop environment "ROX Desktop".                                    |
| [SpaceFM](https://github.com/IgnorantGuru/spacefm)    | 1.0.6           | SpaceFM              | SpaceFM is a file manager on Linux.                                                                         |
| [Thunar](https://gitlab.xfce.org/xfce/thunar)         | 1.0.1 - 1.6.10  | Thunar               | It is the default choice for Xfce-based distributions.                                                      |
| [Xfe](https://sourceforge.net/projects/xfe/)          | 1.37 - 1.43.2   | Xfe                  | X File Explorer (Xfe) is a file manager on Linux.                                                           |
| [zzzFM](https://gitlab.com/antix-contribs/zzzfm/)     | 1.0.7           | zzzFM                | A file manager for the antiX Linux                                                                          |


## Get started

### Download the latest installation script

Go to https://github.com/jonelo/jacksum-fbi-linux/releases and download the .tar.bz2 file.

### Extract the installation script

On most GNU/Linux derivates, and on macOS you can enter
```
$ tar xfvj jacksum*.tar.bz2 ; cd jacksum-file-browser-integration/
```

On most Unix derivates, such as Sun/Oracle Solaris you can enter
```
$ bunzip2 < jacksum*.tar.bz2 | tar xfv - ; cd jacksum-file-browser-integration/
```

### Start the installation script

The installation script is an interactive text user interface that allows you to install Jacksum and HashGarten in your file manager. It also allows uninstalling it again safely and completely. You can run the script as often as you want. If a file manager is not detected on your system, it is marked as DISABLED.

```
$ ./jacksum-file-browser-integration.sh
          >>> Jacksum/HashGarten File Browser Integration v2.4.0 <<<
                            https://jacksum.net

Info:
  If you want to install Jacksum/HashGarten in Dolphin, Konqueror, or Krusader
  for all users, please run this script as root.
--------------------------------------------------------------------------------
Menu:
  1 - Install    in Dolphin, Konqueror, or Krusader for user johann 
  2 - Install    in GNOME Files (Nautilus) for user johann (DISABLED)
  3 - Install    in ROX-Filer for user johann (DISABLED)
  4 - Install    in Thunar for user johann (DISABLED)
  5 - Install    in Xfe for user johann (DISABLED)
  6 - Install    in Nemo for user johann (DISABLED)
  7 - Install    in Caja for user johann (DISABLED)
  8 - Install    in Elementary Files for user johann 
  9 - Install    in SpaceFM for user johann 

  u - Show the uninstall menu
  q - Quit the installer
--------------------------------------------------------------------------------
Enter option: 9

Current parameters:
  [java]: /usr/bin/java
  [jacksum-3.7.0.jar]: /home/johann/Downloads/jacksum-file-browser-integration/jacksum-3.7.0.jar
  [HashGarten-0.14.0.jar]: /home/johann/Downloads/jacksum-file-browser-integration/HashGarten-0.14.0.jar
  [Viewer]: /usr/bin/zenity
  [Editor]: /usr/bin/gedit
  [direct accessible algorithms]: 


A JDK or JRE is required. If you use a headless JDK/JRE, you cannot use HashGarten which is a GUI for Jacksum.
You could go to https://adoptium.net for example to obtain a full JDK/JRE.

Type the absolute path to "java"
and press "Enter" to continue [/usr/bin/java]: 


The jar files Jacksum, HashGarten, and FlatLaf have to be stored in the same folder. The script won't copy those files anywhere, but during runtime it expects those binaries to be there at the specified location after the installation.

Type the absolute path to "jacksum-3.7.0.jar"
and press "Enter" to continue [/home/johann/Downloads/jacksum-file-browser-integration/jacksum-3.7.0.jar]: 

Type the absolute path to "HashGarten-0.14.0.jar"
and press "Enter" to continue [/home/johann/Downloads/jacksum-file-browser-integration/HashGarten-0.14.0.jar]: 


To view text output, you need to specify a viewer or an editor.

Type the absolute path to "viewer"
and press "Enter" to continue [/usr/bin/zenity]: 


To use the "Edit the script" feature, you need to specify an editor.

Type the absolute path to "editor"
and press "Enter" to continue [/usr/bin/gedit]: 


Do you want to access some algorithms directly without the HashGarten GUI?
Type n to disable direct access to algorithms, type p or any other key to use the previous selection [n]: 

Current parameters:
  [java]: /usr/bin/java
  [jacksum-3.7.0.jar]: /home/johann/Downloads/jacksum-file-browser-integration/jacksum-3.7.0.jar
  [HashGarten-0.14.0.jar]: /home/johann/Downloads/jacksum-file-browser-integration/HashGarten-0.14.0.jar
  [Viewer]: /usr/bin/zenity
  [Editor]: /usr/bin/gedit
  [direct accessible algorithms]: 

Do you want to use the parameters above? [y]: 


  Removing jacksum.sh:                [ NOT INSTALLED ]
  Removing jacksum scripts:           [ NOT INSTALLED ]
  Found Jacksum 3.7.0:                [  OK  ]
  Installing jacksum.sh:              [  OK  ]
  Note: Please close all SpaceFM instances manually.
        Please hit any key when you are ready: 
  Creating a folder for all scripts:  [  OK  ]
  Installing scripts:                 [  OK  ]

Installation finished.
Press any key to continue ...
```

## FAQs

### Where can I file bugs, feature requests, and support requests?

Please go to https://github.com/jonelo/jacksum-fbi-linux/issues


### I have installed Krusader, but the installer marked it as DISABLED

On systems without KDE, you need to install both the krusader and the kf5-config package in order to make it work.


### The installer marked all entries as DISABLED

Most likely, you are running a non-supported file manager. If you think it should be supported, please file a feature request.
Please note that the file browser must support sending highlighted files or directories or selected files or directories to a 3rd party application such as a script.


### How do I get the latest Java?

#### Debian based Linux (e.g. Ubuntu)

```
$ sudo apt install openjdk-17-jre
```

You just need to enter `/usr/bin/java` (or hit Enter) if the `jacksum-file-browser-integration.sh` asks you for the java command:
```
$ ./jacksum-file-browser-integration.sh
...
Type the absolute path to "java"
and press "Enter" to continue [/usr/bin/java]: 
```

#### Other Linux

You could use the `update_jdk` script from the [bashberries](https://github.com/jonelo/bashberries) project in order to get a suitable JDK. The following example downloads Temurin 17 (that is the JDK 17 from adoptium), and installs it to `/opt/java/jdk_latest`:
```
$ sudo ./update_jdk -s "https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz" -t jdk /opt/java
```
You just need to enter `/opt/java/jdk_latest/bin/java` if the `jacksum-file-browser-integration.sh` asks you for the java command:

```
$ ./jacksum-file-browser-integration.sh
...
Type the absolute path to "java"
and press "Enter" to continue [/usr/bin/java]: /opt/java/jdk_latest/bin/java
```


## Further hints

For more information about Jacksum see also https://jacksum.net or https://github.com/jonelo/jacksum

For more information about HashGarten see also https://jacksum.net or https://github.com/jonelo/HashGarten

There are also File Browser Integration scripts available for both Microsoft Windows, see also https://github.com/jonelo/jacksum-fbi-windows, and macOS, see also https://github.com/jonelo/jacksum-fbi-macos
