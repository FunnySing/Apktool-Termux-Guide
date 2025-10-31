## Step-by-step guide:


1. Install Termux from f-droid (and enable Internet connection for it.)
2. Run ``cd $HOME`` if you are not in the home directory.
3. Run ``apt update && apt upgrade``
4. Install openjdk and qemu: ``pkg install openjdk-21 zipalign apksigner qemu-user-x86-64``
5. Download the latest Apktool script for linux from its official github repo: ``curl -LO https://raw.githubusercontent.com/iBotPeaches/Apktool/main/scripts/linux/apktool``
6. Move it to Termux user bin folder: ``mv apktool $PATH`` or ``mv apktool $HOME/../usr/bin``
7. Execute it: ``chmod +x $PATH/apktool``
8. Download the latest Apktool jar file from its official release section: ``curl -LO https://github.com/iBotPeaches/Apktool/releases/download/v2.12.1/apktool_2.12.1.jar``
9. Rename it to "apktool.jar": ``mv apktool_2.12.1 apktool.jar``
10. Copy it **(because we will need it later)** to Termux user bin folder: ``cp apktool.jar $PATH``
11. Execute it: ``chmod +r $PATH/apktool.jar``
12. Run this: ``jar -xvf ./apktool.jar prebuilt/linux/aapt2_64``
13. run ``cd prebuilt/linux``
14. Rename it to elf: ``mv aapt2_64 aapt2_64.elf``
15. Open nano: ``nano aapt2_64``
16. Copy the bash script code from [Here](https://github.com/FunnySing/Apktool-Termux-Guide/blob/main/aapt2_64) and paste it.
17. Save it.
18. Now execute it: ``chmod a+x aapt2_64 aapt2_64.elf``
19. Done!

 **Now you can run Apktool by specifying path to aapt2 qemu-user wrapper:**
For example: ``apktool b -a ~/prebuilt/linux/aapt2_64``

📌 Tips: You can write a bash script to make the whole process easy for you.

Credit: [Hytht](https://www.reddit.com/user/Hytht/)


## License
Apache License, Version 2.0
