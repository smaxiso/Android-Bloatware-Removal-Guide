# Android-Bloatware-Removal-Guide
A comprehensive guide on identifying and removing bloatware from Android devices. Learn how to reclaim storage space, improve device performance, and customize your Android experience by removing unnecessary pre-installed apps. This repository includes step-by-step instructions, ADB commands, and tips to help you declutter your Android device efficiently.

<!-- Requirements -->
<h2>Requirements</h2>
<ul>
    <li>An Android phone with Developer Options and USB Debugging enabled.
    <em>Ensure you have the appropriate USB driver installed for your Android device. You can use the <a href="https://adb.clockworkmod.com/">Universal ADB Driver</a> if needed.</em>
    </li>
    <li>A computer or laptop with Windows, macOS or Linux to set up ADB.</li>
    <li>A list of apps/bloatware you wish to uninstall.</li>
</ul>

<!-- Enable Developer Options & USB Debugging -->
<h2>USB Debugging Setup Guide for the Android Device</h2>
<ol>
    <li>Install the USB driver specific to your phone or the Universal ADB Driver.</li>
    <li>On your Android device, navigate to <code>Settings</code> > <code>About Phone</code>. Locate the <code>Build Number</code> and tap it seven times. This action enables Developer Options.</li>
    <li>Access the <code>System</code> settings and then go to <code>Developer Options</code>. Here, find the <code>USB debugging</code> setting and enable it.</li>
</ol>

<br><hr>
<p>Once USB Debugging is set up on the phone, you can follow the instructions in the subsequent sections to setup ADB in the laptop/computer.</p>
<hr><br>

<!-- ADB Setup Guide -->
<h2>ADB Setup Guide for Laptop/Computer</h2>

<p>Follow these instructions to set up ADB on your computer, depending on your operating system.</p>

<!-- Windows -->
<h3>For Windows:</h3>
<ol>
    <li>Download the Android SDK Platform Tools ZIP file for Windows from the following link: <a href="https://dl.google.com/android/repository/platform-tools-latest-windows.zip">Windows ZIP</a>.</li>
    <li>
        <p>Extract the contents of this ZIP file into an easily accessible folder, such as <code>C:\platform-tools</code>.</p>
    </li>
    <li>
        <p>Open File Explorer and browse to where you extracted the contents of this ZIP file.</p>
    </li>
    <li>
        <p>Open a Command Prompt or PowerShell instance from the same directory as this ADB executable. You can do this by holding Shift and right-clicking within the folder, then selecting either "Open command window here" or "Open PowerShell window here." Windows 11 users should see "Open in Terminal" in the right-click context menu without pressing the Shift button.</p>
    </li>
    <li>
        <p>Connect your smartphone or tablet to your computer with a USB cable. Change the USB mode to <code>file transfer (MTP)</code> mode. Some OEMs may or may not require this, but it's best to leave it in this mode for general compatibility.</p>
    </li>
    <li>
        <p>In the Command Prompt or Terminal window, enter the following command to launch the ADB daemon:</p>
        <pre><code>adb devices</code></pre>
    </li>
    <li>
        <p>On your phone's screen, you should see a prompt to allow or deny USB Debugging access. Grant USB Debugging access when prompted (and check the "always allow" option if you want to avoid this prompt in the future).</p>
    </li>
    <li>
        <p>Re-enter the command from step 6. If everything was successful, you should now see your device's serial number in the Command Prompt or Terminal window.</p>
    </li>
</ol>

<p>You can now run any ADB command on your device. Enjoy modding your phone!</p>

<p><em>Note:</em> There are various CLI package managers for Windows, such as WinGet, Scoop, and Chocolatey, that can simplify ADB installation. If you use one of these package managers, you may not need to manually download and update Google's Platform Tools. Keep in mind that version compatibility and installation processes may vary across these package managers, so consult their help manuals and product forums for support.</p>


<!-- macOS -->
<h3>For macOS:</h3>
<ol>
    <li>Download the Android SDK Platform Tools ZIP file for macOS from the following link: <a href="https://dl.google.com/android/repository/platform-tools-latest-darwin.zip">macOS ZIP</a>.</li>
    <li>
        <p>Extract the ZIP to an easily accessible location, such as the Desktop.</p>
    </li>
    <li>
        <p>Open Terminal.</p>
    </li>
    <li>
        <p>To browse to the folder you extracted ADB into, enter the following command:</p>
        <pre><code>cd /path/to/extracted/folder/</code></pre>
        <p>For example, if you placed the contents on your desktop:</p>
        <pre><code>cd /Users/smaxiso/Desktop/platform-tools/</code></pre>
    </li>
    <li>
        <p>Connect your device to your Mac with a compatible USB cable. Change the USB connection mode to <code>file transfer (MTP)</code> mode. This is not always required for every device, but it's best to leave it in this mode to avoid any potential issues.</p>
    </li>
    <li>
        <p>Once the Terminal is in the same folder as your ADB tools, execute the following command to launch the ADB daemon:</p>
        <pre><code>./adb devices</code></pre>
    </li>
    <li>
        <p>On your device, you'll see an Allow USB debugging prompt. Allow the connection.</p>
    </li>
    <li>
        <p>Re-enter the command from step 7. If everything was successful, you should now see your device's serial number in macOS's Terminal window.</p>
    </li>
</ol>

<p>Congratulations! You can now run any ADB command on your device!</p>

<p><em>Note:</em> While the guide above will certainly work, veteran macOS users can also opt to install ADB on their Macs using an unofficial package manager such as Homebrew or MacPorts. This way, you won't have to manually update the binaries.</p>

<!-- Linux -->
<h3>For Linux:</h3>
<ol>
    <li>Download the Android SDK Platform Tools ZIP file for Linux from the following link: <a href="https://dl.google.com/android/repository/platform-tools-latest-linux.zip">Linux ZIP</a>.</li>
    <li>
        <p>Extract the ZIP to an easily accessible location, such as the Desktop.</p>
    </li>
    <li>
        <p>Open a Terminal window.</p>
    </li>
    <li>
        <p>Enter the following command:</p>
        <pre><code>cd /path/to/extracted/folder/</code></pre>
        <p>This will change the directory to where you extracted the ADB files.</p>
        <p>Example:</p>
        <pre><code>cd /home/XDA/Desktop/platform-tools/</code></pre>
    </li>
    <li>
        <p>Connect your device to your Linux machine with your USB cable. Change the connection mode to <code>file transfer (MTP)</code> mode. This is not always necessary for every device, but it's recommended to avoid potential issues.</p>
    </li>
    <li>
        <p>Once the Terminal is in the same folder as your ADB tools, execute the following command to launch the ADB daemon:</p>
        <pre><code>./adb devices</code></pre>
    </li>
    <li>
        <p>Back on your smartphone or tablet device, you'll see a prompt asking you to allow USB debugging. Go ahead and grant it.</p>
    </li>
    <li>
        <p>Re-enter the command from step 7. If everything was successful, you should now see your device's serial number in the Terminal window output.</p>
    </li>
</ol>

<p>Congrats! You can now run any ADB command on your device!</p>

<p><em>Note:</em> Linux users should know that there is an easier way to install ADB on their computers. The guide above will certainly work for you, but those who own a mainstream Debian/Ubuntu or Fedora/SUSE-based distro of Linux can skip steps 1 and 2 of the guide above and use one of the following commands:</p>

<p><strong>Debian/Ubuntu-based Linux users:</strong> You can type the following command to install ADB:</p>
<pre><code>sudo apt-get install android-sdk-platform-tools</code></pre>

<p><strong>Fedora/SUSE-based Linux users:</strong> You can type the following command to install ADB:</p>
<pre><code>sudo dnf install android-tools</code></pre>

<p>However, it is always better to opt for the latest binary from the Android SDK Platform Tools release since the distro-specific packages often contain outdated builds.</p>

<br><hr>
<p>Once ADB is set up, you can follow the instructions in the subsequent sections to find the apps or bloatware to uninstall them.</p>
<hr><br>

<!-- Find Bloatware/Apps for Removal -->
<h2>Find Bloatware/Apps for Removal</h2>

<p>Before uninstalling any apps from your Android device, it's important to identify bloatware or unnecessary apps. Follow these steps to locate and assess apps that you may want to remove:</p>

<ol>
    <li>
        <strong>Check the App Drawer:</strong>
        <p>Start by browsing through your app drawer. Look for apps with unfamiliar or unnecessary names. These are often bloatware apps that come pre-installed on your device.</p>
    </li>
    <li>
        <strong>System Settings:</strong>
        <p>Access your device's settings and navigate to the list of all installed apps. Examine this list for apps you consider bloatware.</p>
    </li>
    <li>
        <strong>Use a Bloatware Scanner App:</strong>
        <p>Explore apps available on the Google Play Store that are designed to identify bloatware. Consider using apps like "Debloater" or "NoBloat Free."</p>
    </li>
    <li>
        <strong>Research Online:</strong>
        <p>Search online for lists of common bloatware apps that come pre-installed on your device's make and model. This research can provide valuable insights into identifying unnecessary apps.</p>
    </li>
    <li>
        <strong>Consult Forums and Communities:</strong>
        <p>Participate in online forums and communities dedicated to Android devices. Engage in discussions about bloatware and seek recommendations for removal.</p>
    </li>
    <li>
        <strong>Use ADB:</strong>
        <p>In the command prompt/terminal window, enter <code>adb shell</code> and hit Enter. Then, use the following command:</p>
        <pre><code>pm list packages | grep '&lt;OEM/Carrier/App Name&gt;'</code></pre>
        <p>This will list all the OEM and carrier apps installed on your device.</p>
    </li>
    <li>
        <strong>App Inspector:</strong>
        <p>Alternatively, you can also use an app called "App Inspector" from the Play Store to know the package names of all the installed apps on your phone. Install the app, select the app you want to uninstall, and the package name will be listed there. Note the package names of all the apps you want to uninstall.</p>
    </li>
</ol>

<p>These steps will help you pinpoint apps that you may consider bloatware. It's crucial to be cautious when removing apps, as some system apps may be critical for your device's functionality. Always back up your device before making any changes and conduct research to ensure the apps you plan to remove are indeed bloatware and not necessary for the device's operation.</p>


<br><hr>
<p>Once the list of apps and bloatware is finalized, you can follow the instructions in the subsequent sections to uninstall apps or bloatware.</p>
<hr><br>

<!-- Uninstall Apps -->
<h2>Uninstall Apps</h2>

<p>Follow these steps to uninstall unwanted apps from your Android device:</p>

<ol>
    <li>
        <p>Open an ADB shell by typing the following command and pressing Enter:</p>
        <pre>adb shell</pre>
    </li>
    <li>
        <p>To uninstall an app (for example, "YouTube"), execute one of the following commands and press Enter:</p>
        <ul>
            <li>
                <p><strong>Command 1:</strong> Uninstall the app while keeping its data and cache:</p>
                <pre>pm uninstall -k --user 0 com.google.android.youtube</pre>
            </li>
            <li>
                <p><strong>Command 2:</strong> Completely uninstall the app, including its data and cache:</p>
                <pre>pm uninstall --user 0 com.google.android.youtube</pre>
            </li>
        </ul>
    </li>
</ol>

<p>After running one of these commands, the specified app will be uninstalled from your device. Choose between Command 1 or Command 2 based on whether you want to keep the app's data and cache or completely remove them.</p>


<p>Replace "<code>com.google.android.youtube</code>" with the package name of the app you want to remove.</p>

<!-- Caution Message -->
<div class="caution-message">
    <p>⚠️ <strong>Caution:</strong> Removing a system app may cause your phone to work improperly and lead to issues. Be extremely cautious before removing any system app and make sure that its removal won't affect the normal functioning of your device.</p>
</div>

<br><hr>
<p>If you wish to reinstall the app which you recently uninstalled, you can follow the instructions in the subsequent sections to reinstall the app.</p>
<hr><br>

<!-- Re-install Apps -->
<h2>Re-install Apps</h2>

<p>Should you ever need to reinstall a previously removed app on your Android device, follow these steps:</p>

<ol>
    <li>
        <p>Start an ADB shell by typing the following command and pressing Enter:</p>
        <pre> adb shell </pre>
    </li>
    <li>
        <p>To re-install an app (for example, "YouTube"), execute one of the following commands based on your preference and press Enter:</p>
        <ul>
            <li>
                <pre>cmd package install-existing com.google.android.youtube</pre>
                <p>This command uses the "cmd" tool to install an existing package (in this case, "com.google.android.youtube," which is the package name for the YouTube app) on an Android device. The "cmd" tool is often used to run Android Debug Bridge (ADB) shell commands from a Windows Command Prompt or terminal. It provides a specific way of installing or reinstalling an app using ADB.</p>
            </li>
            <li>
                <pre>pm install-existing com.google.android.youtube:</pre>
                <p>This command uses the "pm" tool, which stands for "package manager." It's a command-line tool in Android for managing packages (apps). The "pm install-existing" command is used to install an existing package (app) on the device. You would replace "com.google.android.youtube" with the actual package name of the app you want to install or reinstall.</p>
            </li>
        </ul>
    </li>
</ol>

<p>After running these commands, the specified app will be reinstalled on your device. Replace "com.google.android.youtube" with the package name of the app you want to reinstall.</p>




<!-- Support -->
<h2>Support</h2>
<p>If you find this guide helpful and would like to support my work, you can buy me a coffee or donate through PayPal:</p>
<p align="center">
    <a href="https://www.buymeacoffee.com/smaxiso" alt="Buy Me a Coffee">
        <img src="https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black">
    </a>
    &emsp;
    <a href="https://paypal.me/sumitrjk?country.x=IN&locale.x=en_GB" alt="PayPal">
        <img src="https://img.shields.io/badge/PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white">
    </a>
</p>
<br />
<p>And you can reach out to me or follow me here:</p>
<hr />
<!-- Social Media Links -->
<p align="center">
    <a href="https://facebook.com/smaxiso" alt="Facebook">
        <img src="https://img.shields.io/badge/Facebook-%231877F2.svg?style=for-the-badge&logo=Facebook&logoColor=white">
    </a> &bull;
    <a href="https://instagram.com/smaxiso" alt="Instagram">
        <img src="https://img.shields.io/badge/Instagram-%23E4405F.svg?style=for-the-badge&logo=Instagram&logoColor=white">
    </a> &bull;
    <a href="https://github.com/smaxiso" alt="GitHub">
        <img src="https://img.shields.io/badge/github-121013?style=for-the-badge&logo=github&logoColor=white">
    </a> &bull;
    <a href="https://smaxiso.medium.com" alt="Medium">
        <img src="https://img.shields.io/badge/Medium-12100E?style=for-the-badge&logo=medium&logoColor=white">
    </a> &bull;
    <a href="https://twitter.com/smaxiso" alt="Twitter">
        <img src="https://img.shields.io/badge/Twitter-%231DA1F2.svg?style=for-the-badge&logo=Twitter&logoColor=white">
    </a> &bull;
    <a href="https://snapchat.com/add/smaxiso" alt="Snapchat">
        <img src="https://img.shields.io/badge/Snapchat-%23FFFC00.svg?style=for-the-badge&logo=Snapchat&logoColor=white">
    </a> 
</p>

