# Publishing to the Google Play Store with PWABuilder

PWABuilder’s Android platform utilizes the [Bubblewrap tool](https://github.com/GoogleChromeLabs/bubblewrap) to generate a [Trusted Web Activity (TWA)](https://developer.chrome.com/docs/android/trusted-web-activity/) that can be installed on the Google Play Store. This TWA behaves like any other Android application and is a great way to ship your PWA to the Google Play Store.

## Packaging your PWA with PWABuilder

The first step is to generate your Android package with PWABuilder.

1. Navigate to PWABuilder.com.
2. Enter the URL of your PWA on the homepage.

<div class="docs-image">
    <img src="/assets/builder/ios/enter-url.png" width=450>
</div>

3. Click `Next` to navigate to the package selection page.
4. You can now tap the Store Package button on the Android platform to generate your Android app.
5. Click on `Store Package` in the Android section.
   
<div class="docs-image">
    <img src="/assets/builder/ios/ios-publish-section.png" width=550>
</div>

5. Next you will see a list of the different options for the Android platform that are covered in more detail below.
6. When you are ready, tap the Generate button to generate your Android app, and then the Download button when it pops up to download the generated App and associated files.

## Customize your Android package
* Package ID: The Android identifier unique to your app
* App name: The full name of your app. We prepopulate this with the app name from your PWA’s app manifest.
* Launcher name: The name of your app in the Android launcher. This is typically the same as app name, or a shortened version of it. We prepopulate this with short_name from your PWA’s app manifest.
* App version: This is the version string displayed to end users, e.g. “1.0.0.0”
* App version code: This is an integer used as a private, internal version of your app.
* Host, Start URL, Manifest URL: The URLs used to launch your PWA in the Android app. We prepopulate these for you from your app manifest.
* Theme color: The theme color used for the Android status bar in your app. Typically, this should be set to your manifest's theme_color.
* Background color: The background color to use for your app's splash screen. Typically this is set to your manifest's background_color.
* Nav color: The background color to use for your app's splash screen. Typically this is set to your manifest's background_color.
* Nav dark color: The color of the Android navigation bar in your app when the Android device is in dark mode.
* Nav divider color: The color of the Android navigation bar divider in your app.
* Nav divider dark color: The color of the Android navigation bar divider in your app when the Android device is in dark mode.
* Icon URL: The URL to a square PNG image to use for your app's icon. Can be absolute or relative to your manifest. Google recommends a 512x512 PNG without shadows.
* Maskable icon URL: Optional. The URL to a PNG image with a minimum safe zone of trimmable padding, enabling rounded icons on certain Android versions. Google recommends a 512x512 PNG without shadows.
* Monochrome icon URL: Optional. The URL to a PNG image containing only white and black colors, enabling Android to fill the icon with user-specified color or gradient depending on theme, color mode, or Android ontrast settings.
* Manifest URL: The absolute URL of your web manifest.
* Splash fade out duration (ms): How long the splash screen fade out animation should last in milliseconds.
* Fallback behavior:  When the full TWA experience isn’t available, how should your app proceed, whether with a web view or [Chrome’s Custom Tabs](https://developer.chrome.com/docs/android/custom-tabs/) feature. We default to the latter.
* Display mode: \
  - Standalone means your PWA takes up all the area except Android status bar and Navigation bar.
  - Fullscreen hide both bars. This is intended for immersive experiences likes games and media playback.
* Notifications: If enabled, your PWA will use Android Notification Delegation for push notifications, meaning your installed PWA can send push notifications without browser permission prompts. You should enable this if your PWA sends push notifications.
* Notification delegation: If enabled, your PWA can send push notifications without browser permission prompts.
* Location delegation: If enabled, your PWA can access navigator.geolocation without browser permission prompts.
* Google Play billing: If enabled, your PWA can sell in-app purchases and subscriptions via the Digital Goods API.
* Settings shortcut: If enabled, users can long-press on your app tile and a Settings menu item will appear, letting users manage space for your app.
* ChromeOS only: If enabled, your Android package will only run on ChromeOS devices.
* Include source code: If enabled, your download will include the source code for your Android app.
* Signing key: How the APK app package will be digitally signed:
 - None: your app package won’t be signed. Unsigned packages will be signed by the Google Play Store. This is Google’s recommendation, and our default.
 - New: PWABuilder will create a new signing key for you. The signing key will be included in your zip download. Choosing this will let you fill in details like password, alias, and more.
 -  Mine: Upload an existing .keystore file to use for signing the app package. This should be used if you are updating an existing app in the Store. You’ll be prompted to specify your existing key passwords and alias.
* 
