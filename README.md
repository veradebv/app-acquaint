# Acquaint

This is a fork from a prebuilt simple Xamarin app *Acquaint* featured on [Xamarin's Website](https://www.xamarin.com/prebuilt). The app is a simple list of contacts, each of which can be viewed in a detail screen and modified in an edit screen. It runs on iOS 9+, Android 4.2+, and UWP (mobile and desktop).

<img src="https://github.com/xamarinhq/app-acquaint/blob/master/Screenshots/AllScreens_AllPlatforms.jpg" />

## Cross-platform and native

The app is implemented in two ways in order to demonstrate the two different approaches to Xamarin app development:
* Xamarin.Forms cross-platform UI
* Xamarin native, with platform-specific UI implementations

## Platforms

The app targets three platforms:
* iOS
   * Native and Forms version
* Android
   * Native and Forms version
* Universal Windows Platform (UWP)
    * Forms version only
    
## Integrations

Includes integrations available on the detail such as:
* getting directions
* making calls
* sending text messages
* email composition

## Screens

The app has three main screens:
* a list screen
* a read-only detail screen
* an editable detail screen

## Prequisites
* [Visual Studio](https://www.visualstudio.com/) (14.0 or higher) to compile C# 6 langage features (or Visual Studio for Mac)
* Xamarin and UWP add-ons and components for Visual Studio (available via the Visual Studio installer)

## Google Maps API key (Android)
For Android, you'll need to obtain a Google Maps API key:
https://developer.xamarin.com/guides/android/platform_features/maps_and_location/maps/obtaining_a_google_maps_api_key/

Insert it in the Android project: `~/Properties/AndroidManifest.xml`:

    <application ...>
      ...
      <meta-data android:name="com.google.android.geo.API_KEY" android:value="GOOGLE_MAPS_API_KEY" />
      ...
    </application>

## Enabling SQLite for UWP

The UWP app requires that you install the SQLite for UWP extension for Visual Studio. You can find the latest version here:
https://visualstudiogallery.msdn.microsoft.com/4913e7d5-96c9-4dde-a1a1-69820d615936

The steps that were taken to implement it in the UWP project can be found in steps 1-3 here:
https://azure.microsoft.com/en-us/documentation/articles/app-service-mobile-windows-store-dotnet-get-started-offline-data/#_update-the-client-app-to-support-offline-features

## Platform-specific UI Features (in native version only)
| 3D Touch Previewing (iOS) | Shared View Transitions (Android) |
| --- | --- |
| <img src="https://github.com/xamarinhq/app-acquaint/blob/master/Screenshots/Acquaint_N_3DTouch.gif" width="300" /> | <img src="https://github.com/xamarinhq/app-acquaint/blob/master/Screenshots/Acquaint_N_SharedViewTransitions.gif" width="300" /> |

## People

All images of people in the app come from [UIFaces.com](http://uifaces.com/authorized). In accordance with the guidelines, fictitious names have been provided. 

## Troubleshooting
If you encountered "XamlCTask" task could not be initialized with its input parameters, you can try to:
* Updating NuGet Packages and rebuild solution
* Remove all "bin" and "obj" folders and rebuild solution

If there are missing dependencies, you could try to:
* Open NuGet Package Manager for each Projects and let it download missing dependencies by itself
* Open NuGet Package Manager and retrieve missing dependencies manually

If anything else, you could always try to close all instances of Visual Studio and then restart your Visual Studio.
