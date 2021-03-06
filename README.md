Simple SPK Server
=================

Customized version of a very simple Synology Package Server, reverse engineered from
the official Synology package repository and SynoCommunity.

This php script will serve SPKs to a Synology Package Center
while also offering regular HTTP browsing through the available
SPKs.

Customization
=============

- Cache is refreshed as soon as a new version of a package is available.
- Add a fake Synology model 'Any' to be able to display info for the complete list of Packages.
- A new theme 'beatificabytes' has been added.
- An opened lock is displayed on the logo of each unsigned packages.
- Clicking on that lock will sign the package if sspks was installed with my own SPK (MODS_SSPKS)
- A camera is displayed on the logo of each package having snapshots.
- Clicking on that camera will display the snapshots.

MODS_SSPKS.spk
==============

My own spk created with these sources and Mods Packager can be found ![here](https://github.com/vletroye/SynoPackages/tree/master/MODS%20Simple%20SPK%20Server)

This spk will:
- prompt the user to pick a theme during installation
- prompt the user to get name and email in order to create gpgkeys
- create gpg keys for package signing purpose (gpg2 - gpgme - me needs to be installed on Synology)
- publish the public key in SSPKS so users can trust packages signed there


Installation
============

This code is used as-is by "Mods Packager" to create a SPK file that can be deployed on Synology.
You will have to install gpg2 on your synology using the following command in a ssh console: ipkg install gpgme

Contribute
==========

This is a fork version of the original sspks to be found on https://github.com/jdel/sspks.git
