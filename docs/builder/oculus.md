# Creating Packages for 

PWABuilder’s Android platform utilizes the [Bubblewrap tool](https://github.com/GoogleChromeLabs/bubblewrap) to generate a [Trusted Web Activity (TWA)](https://developer.chrome.com/docs/android/trusted-web-activity/) that can be installed on the Google Play Store. This TWA behaves like any other Android application and is a great way to ship your PWA to the Google Play Store.

## Prerequisites

We strongly recommend reading Meta's documentation on PWAs:
- [Overview of PWA support on Meta Quest 2](https://developer.oculus.com/pwa/)

You will need: 
* A valid PWA with a web manifest, published to the web and secured through HTTPS
* An Oculus Quest 2 for sideloading and testing
* An Oculus Developer Account and Device Setup (follow instructions [here](https://developer.oculus.com/documentation/native/android/mobile-device-setup/))

## Packaging your PWA with PWABuilder

The first step is to generate your .apk package with PWABuilder.

1. Navigate to preview.PWABuilder.com.
2. Enter the URL of your PWA on the homepage.

<div class="docs-image">
    <img src="../assets/builder/oculus/url.jpg" width=450>
</div>

3. Click `Next` to navigate to the package selection page.
4. Click on `Store Package` in the Oculus section.
   
<div class="docs-image">
    <img src="../assets/builder/oculus/store_package.jpg" width=550>
</div>

5. Next you will see a list of the different options for the Meta Quest platform that are covered in more detail below.
6. When you are ready, tap the Generate button to generate your Oculus app package, and then the Download button when it pops up to download the generated App and associated files.

## Customize your .apk package
* Package ID: The ID of your Meta Quest app. We recommend a reverse-domain style string: com.domainname.appname. Letters, numbers, periods, hyphens, and underscores are allowed.
* App name: The name of your app as displayed to users.
* Launcher name: The name of your app in the Android launcher. This is typically the same as app name, or a shortened version of it. We prepopulate this with 
* App version: This is the version string displayed to end users, e.g. “1.0.0.0”
* App version code: This is an integer used as a private, internal version of your app.
* Manifest URL: The URL of your app manifest. We prepopulate this for you.
* Signing key: How the APK app package will be digitally signed:
  - None: your app package won’t be signed. 
  - New: PWABuilder will create a new signing key for you. The signing key will be included in your zip download. Choosing this will let you fill in details like password, alias, and more.
  - Mine: Upload an existing .keystore file to use for signing the app package. This should be used if you are updating an existing app. You’ll be prompted to specify your existing key passwords and alias.

    
## Save your signing key
Your zip file contains ```signing.keystore``` and ```signing-key-info.txt```. ```signing.keystore``` is the key store file containing the signing key.
```signing-key-info.txt``` is a text file containing your signing key information, such as the key password, store password, and key alias.
Keep both of these files in a safe place. You’ll need them to deploy future versions of your app. 

## Sideloading and Testing your app on your Meta Quest 2 device

For this step, you'll need:

- A Meta Quest 2 device
- A USB-C cable to connect your Meta Quest 2 device to your PC or Mac
- Verify your Quest software is up-to-date. Turn on your Oculus device and open `Settings` -> `System` -> `Software Update`.  Your software version should be 31 or greater.
- Make sure your device is setup and your developer account is enabled according to the documentation [here](https://developer.oculus.com/documentation/native/android/mobile-device-setup/). 
- Follow the instructions [here](https://developer.oculus.com/documentation/web/pwa-packaging/#sideload-your-pwa-to-test) to sideload and test your app on your Meta Quest 2!
