# Android-Bloatware-Removal-Guide
A comprehensive guide on identifying and removing bloatware from Android devices. Learn how to reclaim storage space, improve device performance, and customize your Android experience by removing unnecessary pre-installed apps. This repository includes step-by-step instructions, ADB commands, and tips to help you declutter your Android device efficiently.

<!-- Requirements -->
<h2>Requirements</h2>
<ul>
    <li>Your computer should run the Windows operating system.</li>
    <li>Download ADBKit from this <a href="https://github.com/K3V1991/ADBKit">GitHub</a> repository.</li>
    <li>Ensure you have the appropriate USB driver installed for your Android device. You can use the <a href="https://adb.clockworkmod.com/">Universal ADB Driver</a> if needed.</li>
</ul>

<!-- Enable Developer Options & USB Debugging -->
<h2>Enable Developer Options & USB Debugging</h2>
<ol>
    <li>Install the USB driver specific to your phone or the Universal ADB Driver.</li>
    <li>On your Android device, navigate to <code>Settings</code> > <code>About Phone</code>. Locate the <code>Build Number</code> and tap it seven times. This action enables Developer Options.</li>
    <li>Access the <code>System</code> settings and then go to <code>Developer Options</code>. Here, find the <code>USB debugging</code> setting and enable it.</li>
    <li>Connect your Android device to your computer using a USB cable. Ensure that you change the connection mode from <code>Charge only</code> to <code>File Transfer</code>.</li>
    <li>On your computer, navigate to the directory where you've extracted the ADBKit Zip file.</li>
    <li>Launch a Command Prompt by running the <code>Open CMD.bat</code> file.</li>
    <li>Once you are in the Command Prompt, enter the following command:</li>
    <pre> adb devices </pre>
    <li>Your system will start the ADB Daemon. If this is your first time running ADB, a prompt will appear on your Android device asking you to authorize a connection with the computer. Click "OK" to proceed.</li>
    <li>USB debugging has been successfully enabled.</li>
</ol>

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
        <p>Explore apps available on the Google Play Store that are designed to identify the bloatware. Consider using apps like "Debloater" or "NoBloat Free."</p>
    </li>
    <li>
        <strong>Research Online:</strong>
        <p>Search online for lists of common bloatware apps that come pre-installed on your device's make and model. This research can provide valuable insights into identifying unnecessary apps.</p>
    </li>
    <li>
        <strong>Consult Forums and Communities:</strong>
        <p>Participate in online forums and communities dedicated to Android devices. Engage in discussions about bloatware and seek recommendations for removal.</p>
    </li>
</ol>

<p>These steps will help you pinpoint apps that you may consider bloatware. It's crucial to be cautious when removing apps, as some system apps may be critical for your device's functionality. Always back up your device before making any changes and conduct research to ensure the apps you plan to remove are indeed bloatware and not necessary for the device's operation.</p>


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

<!-- Re-install Apps -->
<h2>Re-install Apps</h2>

<p>Should you ever need to reinstall a previously removed app on your Android device, follow these steps:</p>

<ol>
    <li>
        <p>Start an ADB shell by typing the following command and pressing Enter:</p>
        <pre> adb shell </pre>
    </li>
    <li>
        <p>To re-install an app (for example, "YouTube"), execute the following command and press Enter:</p>
        <pre> cmd package install-existing com.google.android.youtube </pre>
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

