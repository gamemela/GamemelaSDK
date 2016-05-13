![Gamemela Logo](docs/images/Gamememla Signature Size Logo.png)
# Gamemela SDK
_Copyright (c) 2016 Funizen Inc. All rights reserved._

## Overview

The GAMEMELA SDK allows you to access the GAMEMELA Services API.
The plugin provides support for the following features of the GAMEMELA API:<br/>
* sign up
* sign in
* sign out

All features are available on Android.

Installation of GamemelaSDK
-----------------------

1. [[Download GamemelaSDK Plugin for Unity.](ARCHIVE.md)]
2. Open your project for Unity.
3. Import downloaded package [gamemela-unity-sdk.x.y.z.unitypackage].
4. Gamemela -> Edit Settings
  * ![MainMenu->Gamemela->Edit Settings](docs/images/GamemelaScreenShot-GamemelaSettings.jpg)

Usage for social features.
-----------------------
### Namespace
	using GamemelaSdk.Unity;

### Initialize
		GM.Init(facebookAppId:"");

### Check sign in
		if (GM.IsSignedIn())
		{
			Debug.Log("Gamemela signed in.");
		}
		else
		{
			Debug.Log("Gamemela signed out.");
		}

### Sign in
		GM.LoadPageSignIn((success, message)=> {
			Debug.Log("OnButtonSignInGamemela: " + success + " / " + message);
		});

### Customer Service
		GM.LoadPageCustomerService();

### Sign out
		GM.SignOut();

# Gamemela Ads
## Overview

The GAMEMELA Ads is integration Ads of UnityAds, InMobi, GoogleAds.
* Banner
* Interstition
* RewardedVideo

All features are available on Android.

Usage for Ads.
-----------------------
### Namespace
	using GamemelaSdk.Unity;

### Settings
		// Unity
		Settings.instance.unity.androidGameId = "xxxxxxx";
		Settings.instance.unity.androidInterstitialPlacementId = "xxxxxxxx";
		Settings.instance.unity.androidRewardedPlacementId = "xxxxxxxx";

		// InMobi
		Settings.instance.inMobi.accountId = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx";
		Settings.instance.inMobi.bannerPlacementId = 000000000000;
		Settings.instance.inMobi.interstitialPlacementId = 00000000000;

		// Google
		Settings.instance.google.adUnitIdBanner = "ca-app-pub-xxxxxxxxxxxxx/xxxxxxxxxxxx";
		Settings.instance.google.adUnitIdInterstitial = "ca-app-pub-xxxxxxxxxxxxx/xxxxxxxxxxxx";
		Settings.instance.google.adUnitIdReward = "ca-app-pub-xxxxxxxxxxxxx/xxxxxxxxxxxx";
### Initialize
		Ads ads = Xxx.instance;
		
		// Xxx have to replace with <AdsUnity, AdsGoogle, AdsInMobi>

### ShowBanner / Destroy Banner
		ads.ShowBanner();

		ads.DestroyBanner();

### ShowInterstitial
		ads.ShowInterstitial();

### ShowRewardedVideo
		ads.ShowRewardedVideo();


# References
-----------------------

_[Facebook SDK for Unity](https://github.com/facebook/facebook-sdk-for-unity)_

_[Google Play Games plugin for Unity](https://github.com/playgameservices/play-games-plugin-for-unity)_

_[Google Analytics Plugin for Unity](https://github.com/googleanalytics/google-analytics-plugin-for-unity)_

_[Google Mobile Ads Unity Plugin](https://github.com/googleads/googleads-mobile-unity)_

_[InMobi Ads Plugin for Unity Guide](https://support.inmobi.com/monetize/integration/partner-platforms/unity-partner-platform-android-integration-guide/) / [Download](https://dl.inmobi.com/SDK/Plugins/InMobi_Unity_Android_Plugin.zip)_

_[unity-webview](https://github.com/gree/unity-webview)_

_[Unity Ads SDK](https://github.com/Applifier/unity-ads-sdk)_

_[Unity HTTP](https://github.com/andyburke/UnityHTTP)_

......


