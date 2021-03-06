## Abstract
Full-fledged WebView as Xamarin.Forms plugin (XLabs based) with cross-platform C# to JavaScript and JavaScript to C# calls support. Built for painless hybrid apps creation.

HybridWebPlatform based on great XLabs core components, but does not depends on [XLabs.HybridWebView](https://github.com/XLabs/Xamarin-Forms-Labs/wiki/HybridWebView). Moreover, HybridWebPlatform replacing XLabs.HybridWebView as more advanced and not legacy plugin.

## HybridWebPlatform Advantages
It solves the following problems for:

- Xamrin.Forms WebView
  - Allows to call C# from JavaScript
- XLabs.WebView
  - Fix rendering perfromance issue on Android (Hardware rendering)

## Road Map
- [ ] Enable Hardware accelaration by default (actual for Android)
- [ ] Support UWP
- [ ] Fix keyboard overlap issue on Android

## How-to Use
1. Install NuGet package for all PCL, Android and iOS projects using e.g. Xamarin Studio. *To install NuGet correctly, make sure you use Profile111 for PCL.*
1. [iOS] Invoke Renderer (TBD)
1. [Android] Add Android.Export (http://stackoverflow.com/questions/31085554/you-need-to-add-a-reference-to-mono-android-export-dll-when-you-use-exportattrib)
1. [Android][Optional] Enable hardware rendering using the following code within _MainActivity.OnCreate()_ class before _LoadApplication()_ invoke.
```
// ...
HybridWebControl.Droid.HybridWebViewRenderer.EnableHardwareRendering = true;
LoadApplication(new App());
```
