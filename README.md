The PhotonAOSP Project
=====================

Getting Started
---------------

To build the PhotonAOSP ROM from source, you'll need to be familiar with
[Git and Repo](http://source.android.com/download/using-repo).


To initialize your local repository, use this command:

	repo init -u https://github.com/PhotonAOSP/platform_manifest.git -b mm6.0
	
Then to sync source, use this command:

	repo sync -j# (# = number of jobs)

After syncing is done, use these commands to build:

	1) source build/envsetup.sh
	2) lunch photon_DEVICE-userdebug
	3) make -j# otapackage (# = number of jobs)

Device Codenames:

	Officially supported devices:
	
		Nexus 6P - angler
		Nexus 5X - bullhead
		Nexus 5 - hammerhead
		Nexus 6 - shamu

Updating and Rebuilding:

	1) repo sync (use "repo sync --foce-sync" if you encounter errors)
	2) make clobber
  
*Substitute "DEVICE" with the appropriate codename
