# Introduction and Installation by Nathan Hostetler

## **<u>Installation notes</u>**

-   FSL is **not** the same thing as FreeSurfer. Their websites look
    similarly rugged, but the “FS” in FSL has nothing to do with
    FreeSurfer. Do not make the same mistake as me and spend a day
    downloading FSL, only to realize that it’s not FreeSurfer.

-   There is a tutorial online suggesting that you need “VirtualBox” to
    run FreeSurfer on Windows – you do not. Disregard that tutorial and
    the ridiculous 60 GB file that comes with it. It will waste a lot of
    your time!

-   **LINK TO YOUTUBE PLAYLIST WITH VIDEOS THAT ACCOMPANY THIS GUIDE:**

    -   [<u>https://youtube.com/playlist?list=PLNDwvfjY9YL2X8MkwrFFORg4qu_2t1OzT</u>](https://youtube.com/playlist?list=PLNDwvfjY9YL2X8MkwrFFORg4qu_2t1OzT)

## **<u>Steps</u>**

### **Video 1 - Enabling “Windows Subsystem for Linux”. [<u>https://youtu.be/ux-C0y-3Qzw</u>](https://youtu.be/ux-C0y-3Qzw)** 

-   Pathway:

    -   1\) Click the “Start” button (windows logo) in the bottom left

    -   2\) Press the gear on the left side of the screen to open
        settings

    -   3\) Click on “apps” or “apps and features” – whichever one you
        see

    -   4\) In the next window, click “programs and features” in the top
        right (the window <u>must</u> be maximized for you to see this)

    -   5\) Click on “Turn Windows features on or off” in the top left

    -   6\) Scroll down in this window until you see “Windows Subsystem
        for Linux”, and check the corresponding box.

    -   7\) Press “OK”.

    -   8\) Select “Restart now”.

-   Relevant YouTube link:

### **Video 2 - Install Ubuntu from the Microsoft Store [<u>https://youtu.be/u-u0ky38T9A</u>](https://youtu.be/u-u0ky38T9A)** 

-   Pathway:

    -   1\) Click the search button (magnifying glass) in the bottom
        left of your screen.

    -   2\) Search “Microsoft Store” and click on it.

    -   3\) Within this window, click on the search tool in the top
        right.

    -   4\) Search “Ubuntu” and click on one of the applications. At
        time of writing there are three: Ubuntu, Ubuntu 20.04 LTS, and
        Ubuntu 18.04 LTS.

        -   I used Ubuntu 18.04 LTS. It worked. I cannot comment on if
            the others do.

    -   5\) On the application page within Microsoft Store, press “Get”
        to install the application.

    -   6\) Upon successful installation, there should be a blue icon
        within the application’s Microsoft Store page that says
        “Launch”. Press this button.

    -   7\) After a few minutes, the program will ask you to make a
        username and password.

        -   **<u>Write down your username and don’t give it any
            spaces.</u>**

### **Video 2 - Configuring Ubuntu [<u>https://youtu.be/u-u0ky38T9A</u>](https://youtu.be/u-u0ky38T9A)** 

-   1\) Copy and paste this into Ubuntu.

    -   ```sudo apt-get update```

    -   The paste button in Ubuntu is a right click.

    -   Do not accidentally include a space after the word “update”.

-   2\) Copy and paste this into Ubuntu.

    -   ```sudo apt-get install tcsh libfreetype6 libglu1-mesa libfontconfig1 libxrender1 libsm6 libxt6```

### **Video 3 and 10 - Install a graphics displayer [<u>https://youtu.be/3K6Z36cYWqo</u>](https://youtu.be/3K6Z36cYWqo) OR [<u>https://youtu.be/RcwKpZDobNA</u>](https://youtu.be/RcwKpZDobNA)** 

-   Click this link:

    -   [<u>https://sourceforge.net/projects/xming/</u>](https://sourceforge.net/projects/xming/)

    -   Press the green “Download” button.

    -   Upon successful download, click on the downloaded application at
        the bottom of your browser or in your “downloads” folder.

        -   It should be called something along the lines of XMing
            setup, with some numbers interspersed. My download was
            called Xming-6-9-0-31-setup.

    -   A prompt will appear: “Do you want to allow this application
        from an unknown publisher to make changes to your computer?”

        -   Select “Yes”.

    -   Keep pressing “Next” within the installation window until you
        see the “Install” button.

    -   When you see the “Install” button, press it.

-   If you are using Windows Subsystem for Linux 2, install this XServer
    instead and see the video titled “Installing a Different XServer”
    for further instruction.

    -   [<u>https://sourceforge.net/projects/vcxsrv/</u>](https://sourceforge.net/projects/vcxsrv/)

    -   You should also install this XServer (instead of XMing) if, when
        launching freeview, Ubuntu reads “failed to get the screen
        resources” or “XCB error”.

### **Video 4 - Downloading FreeSurfer [<u>https://youtu.be/0_lqIT2H_9g</u>](https://youtu.be/0_lqIT2H_9g)** 

-   Click this link
    [<u>https://surfer.nmr.mgh.harvard.edu/fswiki/rel7downloads</u>](https://surfer.nmr.mgh.harvard.edu/fswiki/rel7downloads)

-   Scroll down to the table with headings “**OS Build \| Build Platform
    \| Version etc.**”

-   Find the row that has “CentOS 7 x86_64 (64b) tar archive” listed in
    the “Build Platform” column.

-   Press the download link for that row, under the column “Download”.

    -   The download will be in your downloads folder by default.

-   Launch Ubuntu by searching it and then clicking it (using the
    magnifying glass icon in the bottom left).

-   Copy and paste the following into Ubuntu.

    -   cd /mnt/c/Users/Mauricio/Downloads

        -   Your Windows username is not the same as the Ubuntu username
            you previously created. You can find your Windows user name
            by using Windows file explorer and navigating to This PC 🡪
            Users. Look at the User list, and decide which user you are.

        -   #### If you get the error “No such file or directory found”. (If you do not get this error, close this portion of the document and proceed to “Now, copy and paste …” below)

        -   I had a really weird issue where Ubuntu could not locate my
            user or any of the files I had stored. No matter what I
            tried, Ubuntu insisted that there was “no such file or
            directory” under Users/Nate Hostetler.

            -   If Ubuntu returns you the error “No such file or
                directory found”, there is an interesting way to
                troubleshoot this and determine where the problem lies.
                It is easiest to see this with an example.

                -   As mentioned earlier, my issue was with my User –
                    for some reason, Ubuntu did not think that the user
                    “Nate Hostetler” existed.

                -   Step by step, add more to this phrase until you get
                    an error message. For me, this looked something like
                    this:

                    -   /mnt

                        -   “Is a directory”

                    -   /mnt/c

                        -   “Is a directory”

                    -   /mnt/c/Users

                        -   “Is a directory”

                    -   /mnt/c/Users/Nate Hostetler

                        -   /mnt/c/Users/Nate: No such file or
                            directory.

                -   Now, I knew where the error was. Ubuntu recognized
                    everything until I entered my user’s name. I tried
                    using an underscore/hyphen to separate my first and
                    last name – but nothing worked.

                -   The workaround I ended up using was making an
                    entirely new User on my PC and storing the file
                    there. Then, I routed Ubuntu to this new user
                    instead of to my User. For some reason, Ubuntu
                    recognized this new pathway as valid. This was a
                    long and annoying fix that involved changing
                    permissions and stuff, so just call me if this
                    happens to you and you need help.

                    -   If you want to figure it out on your own, I
                        basically just made a new user and then right
                        clicked on that user in the “Users” tab in file
                        explorer. I then clicked “Give access to”, and
                        gave access to my actual user, the one that was
                        initially giving me all the grief (Nate
                        Hostetler).

                    -   Now, with the downloaded file stored in a
                        location that Ubuntu recognized and that my user
                        had access to, I repeated the step above –
                        guiding Ubuntu to my new user named
                        NateHostetler6.

                        -   cd /mnt/c/Users/NateHostetler6/Downloads

-   #### Now, copy and paste the following into Ubuntu and press enter.

    -   ```sudo tar -zxvf freesurfer-linux-centos7_x86_64-7.1.1.tar.gz```

    -   If it copies into Ubuntu as “otar”, remove the o. It should only
        say tar.

-   Each subsequent step represents a separate “copy + paste into
    Ubuntu”.

    -   1\) ```cd freesurfer```

    -   2\) ```pwd```

    -   3\) ```export FREESURFER_HOME=$HOME/freesurfer```
            ```echo "export FREESURFER_HOME=/mnt/c/Users/Mauricio/Downloads/freesurfer >> $HOME/.bashrc```
            

    -   4\) ```export SUBJECTS_DIR=$FREESURFER_HOME/subjects```

    -   5\) ```source $FREESURFER_HOME/SetUpFreeSurfer.sh```

### **Video 5 - Obtaining a FreeSurfer License [<u>https://youtu.be/1qA3uPUOBRU</u>](https://youtu.be/1qA3uPUOBRU)** 

-   Click this link:

    -   [<u>https://surfer.nmr.mgh.harvard.edu/registration.html</u>](https://surfer.nmr.mgh.harvard.edu/registration.html)

    -   Fill in the information required, pressing agree where
        necessary.

    -   You will receive an email that contains your license file. The
        license file is called “license.txt”.

    -   Open an instance of windows file explorer and press the “View”
        button at the top. Within this “view” pane at the top of the
        file explorer, click “options”. Within the next window, select
        the “view” tab at the top. In the window here, click on “Show
        hidden files, folders, and drives”. Click apply, then OK, and
        then exit the window.

    -   Save the license.txt file from the email to the following
        location:

        -   **This PC 🡪 Users 🡪 Your Windows User’s Name 🡪 AppData 🡪
            Local 🡪 Packages 🡪
            CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc 🡪
            LocalState 🡪 rootfs 🡪 home 🡪 YOUR USERNAME FOR UBUNTU THAT
            YOU WROTE DOWN EARLIER 🡪 freesurfer.**

### Videos 6-8: Launching FreeSurfer

#### **Video 6 “Making FreeSurfer Easier to Launch”**: [<u>https://youtu.be/Yz1QFweMOHM</u>](https://youtu.be/Yz1QFweMOHM) 

-   Open Ubuntu and XMing (your graphics displayer from earlier). To
    open XMing, use the search tool (magnifying glass in the bottom
    left) to search for and click on XLaunch (all the stock settings are
    fine here, just click through).

-   Copy and paste the following into Ubuntu.

    -   ```sudo gedit .bashrc```

-   Scroll to the bottom of the resulting code-filled window. Beneath
    the final line of code, copy and paste the following:

    -   ```alias sfs=’export FREESURFER_HOME=/home/**YOUR UBUNTU USERNAME FROM EARLIER**/freesurfer ; source $FREESURFER_HOME/SetUpFreeSurfer.sh’```

    -   It might not let you paste. Just type it in exactly (letter for
        letter) instead, and replace “YOUR UBUNTU …” with your username.
        For me, this was nhostetl. This is **not the same as your
        windows username. It is the username you wrote down up here .**

-   Close Ubuntu.

-   Reopen Ubuntu.

-   Type sfs into Ubuntu.

-   Type freeview into Ubuntu.

#### Video 7: Only works if you completed the above steps: [<u>https://youtu.be/bYnEwXVHvyA</u>](https://youtu.be/bYnEwXVHvyA) 

Any time you wish to run freesurfer, type sfs first. Then type freeview,
or whatever other command you need. Your steps to run freesurfer

1.  open Ubuntu

2.  Type sfs and press enter

3.  Type freeview, recon-all, whatever else you wanna do.

To open freesurfer, your XMing must be running. If FreeSurfer fails to
open, trying launching XMing through XLaunch (search it and click it),
and then try again.

#### Video 8: without completing the steps listed prior to “Option A” [<u>https://youtu.be/\_pmzJTiSLrU</u>](https://youtu.be/_pmzJTiSLrU) 

-   Open a new instance of Ubuntu.

-   Copy and paste the following into Ubuntu, in order:

    -   1\) ```export SUBJECTS_DIR=$FREESURFER_HOME/subjects```

    -   2\) ```source $FREESURFER_HOME/SetUpFreeSurfer.sh```

-   Now type “freeview”, “recon-all”, or whatever other command you wish
    to run.

### **Video 9 - If you get an error that freeview cannot open, follow the steps provided here: [<u>https://youtu.be/Ruuv5OTE9qo</u>](https://youtu.be/Ruuv5OTE9qo)** 

[<u>https://surfer.nmr.mgh.harvard.edu/fswiki/UpdateFreeview</u>](https://surfer.nmr.mgh.harvard.edu/fswiki/UpdateFreeview)

**<u>Note</u>**: for step 2, you may have to input “sudo” into Ubuntu
before inputting the commands. This would look something like this: (the
website does not normally have sudo in this command)

```**sudo** rm -rf ${FREESURFER_HOME}/lib/qt ${FREESURFER_HOME}/lib/vtk```

```cp -r freesurfer/lib/qt ${FREESURFER_HOME}/lib/qt```

```cp -r freesurfer/lib/vtk ${FREESURFER_HOME}/lib/vtk```

```cp freesurfer/bin/freeview freesurfer/bin/qt.conf ${FREESURFER_HOME}/bin/```

**As a general rule, when Ubuntu tells you that “permission is denied”,
input sudo before the command and see if it works.**

# Resources for Further Learning

-   I am finding FreeSurfer’s website and YouTube channel to be very
    helpful. Specifically, I’m finding the website’s tutorial page to be
    very handy. Here is the link to their tutorial page, and YouTube
    channel (where the videos accompanying the tutorial can be found).

    -   [<u>Freesurfer -
        YouTube</u>](https://www.youtube.com/channel/UCruQerP8aa-gYttXkAcyveA)

    -   [<u>FsTutorial - Free Surfer
        Wiki</u>](https://surfer.nmr.mgh.harvard.edu/fswiki/FsTutorial)

    -   [<u>https://surfer.nmr.mgh.harvard.edu/fswiki/UnixTutorial</u>](https://surfer.nmr.mgh.harvard.edu/fswiki/UnixTutorial)

        -   This link is **<u>incredibly</u>** helpful for learning your
            way around the Linux terminal (the codey aspect of
            FreeSurfer).

-   In addition, I have found Andy’s Brain Blog’s YouTube channel to be
    great. Here is the link:

    -   [<u>https://www.youtube.com/watch?v=6wxJ1up-E7E&list=PLIQIswOrUH6_DWy5mJlSfj6AWY0y9iUce</u>](https://www.youtube.com/watch?v=6wxJ1up-E7E&list=PLIQIswOrUH6_DWy5mJlSfj6AWY0y9iUce)

        -   This is a playlist he has about FreeSurfer. There are other
            videos on his channel that are helpful as well.
