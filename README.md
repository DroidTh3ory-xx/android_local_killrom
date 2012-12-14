android_local_killrom
====================

Local Manifest for KillRom AOSP

Getting Started
---------------

To get started with Android, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).

Make a build directory:

	mkdir Android (or whatever name you choose)
	cd Android (or the name  you chose)
	

To initialize your local repository using the AOSP manifest, use commands like these:

    repo init -u https://android.googlesource.com/platform/manifest -b android-4.2.1_r1

    curl -L -o .repo/local_manifest.xml -O -L https://raw.github.com/DroidTh3ory/android_local_killrom/master/local_manifest.xml

    	( or Download: https://github.com/DroidTh3ory/android_local_killrom/master/local_manifest.xml
		and place it in ~/Android/.repo/local_manifest.xml (or ~/'name you chose'/.repo)

Then sync up and buckle up (It's the law):

    repo sync
    
Then build it:

    . build/envsetup.sh
    lunch
    (choose build)
    make -j8 && make bacon
