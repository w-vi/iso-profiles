iso-profiles
==========================

######* profile.conf

~~~
##########################################
###### use this file in the profile ######
##########################################

# use multilib packages; x86_64 only
# multilib="true"

# use extra packages as defined in pkglist to activate a full profile
# extra="false"

################ install ################

# default displaymanager: none
# supported; lightdm, sddm, gdm, lxdm, mdm
# displaymanager="none"

# Set to false to disable autologin in the livecd
# autologin="true"

# nonfree xorg drivers
# nonfree_mhwd="true"

# configure calamares for netinstall
# netinstall="false"

# configure calamares to use chrootcfg instead of unpackfs; default: unpackfs
# chrootcfg="false"

# unset defaults to given values
# names must match systemd service names
# enable_systemd=('bluetooth' 'cronie' 'ModemManager' 'NetworkManager' 'org.cups.cupsd' 'tlp' 'tlp-sleep')

# unset defaults to given values,
# names must match openrc service names
# enable_openrc=('acpid' 'bluetooth' 'elogind' 'cronie' 'cupsd' 'dbus' 'syslog-ng' 'NetworkManager')

# unset defaults to given values
# addgroups="video,power,disk,storage,optical,network,lp,scanner,wheel"

################# live-session #################

# unset defaults to given value
# hostname="manjaro"

# unset defaults to given value
# username="manjaro"

# unset defaults to given value
# password="manjaro"

# the login shell
# defaults to bash
# login_shell=/bin/bash
~~~

######* New Packagelist tags

~~~
>openrc
>systemd

>i686
>x86_64
>multilib

>nonfree_default
>nonfree_i686
>nonfree_x86_64
>nonfree_multilib

>manjaro
>sonar

>basic
>extra
~~~

######* Packages-Desktop
* Contains the desktop image packages
* desktop environment packages go here

######* Packages-Live
* Contains packages you only want in live session but not installed on the target system with installer


######* buildiso can be configured to use custom repos.

* create a user-repos.conf

~~~
${profile_dir}/user-repos.conf
~~~

Add only your repos to user-repos.conf!

######* Calamares
* netgroups definitions go in [this] (https://github.com/manjaro/calamares-netgroups) repo please
