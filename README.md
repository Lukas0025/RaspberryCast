# RaspberryCast 3.0 (active folk)
> Transform your Raspberry Pi into a streaming device (with working youtube).
Cast videos from mobile devices or computers to your TV.


[![Android app](https://developer.android.com/images/brand/en_app_rgb_wo_60.png)](https://apkcombo.com/raspberrycast/com.kiwiidev.raspberrycast/)
[![Extension for Chrome](https://developer.chrome.com/webstore/images/ChromeWebStore_BadgeWBorder_v2_206x58.png)](https://chrome.google.com/webstore/detail/raspberrycast/aikmhmnmlebhcjjdbjilohbpfljioeak)
[![Extension for Firefox](https://raw.githubusercontent.com/vincelwt/RaspberryCast/master/images/firefox.png)](https://addons.mozilla.org/firefox/addon/raspberrycast/)

## Supported services
Works with all youtube-dl supported websites: http://rg3.github.io/youtube-dl/supportedsites.html (YouTube, SoundCloud, Dailymotion, Vimeo, etc...) and also any direct link to mp3, mp4, avi and mkv file.

You can also cast playlists from Youtube or Soundcloud.

## How to install (Raspberry Pi side)

First install raspberian os with OMXPLAYER (Only older verion of Debian)

```
wget https://raw.githubusercontent.com/Lukas0025/RaspberryCast/master/setup.sh && sudo sh setup.sh
```
That's it.

The installation script will:
- Download RaspberryCast and install the necessary dependencies
- Autostart RaspberryCast at boot (added to /etc/rc.local)
- Reboot

You can review the [install script](https://github.com/Lukas0025/RaspberryCast/blob/master/setup.sh).

# Remote control (mobile devices)
![The remote on Android](https://raw.githubusercontent.com/Lukas0025/RaspberryCast/master/images/android.png)

On any device connected to the same network as you Pi, you can visit the page:
```
http://raspberrypi.local:2020/remote
```
Note that you can "Add to homescreen" this link
 
You can also use the Android application (link to Playstore at the top of the page)

## Chrome & Firefox extension
#### Extension options
![alt tag](https://raw.githubusercontent.com/Lukas0025/RaspberryCast/master/images/extension.png)

#### Right-click options
![alt tag](https://raw.githubusercontent.com/Lukas0025/RaspberryCast/master/images/rightclick.png)

You can configure RaspberryCast settings in the extension option page.

## Cast videos from computer

Works on Linux, Mac OS, and Windows (Python needed)

**Download**

```
wget https://raw.githubusercontent.com/vincelwt/RaspberryCast/master/rcast.py
```

**Usage**

```
python rcast.py video.mkv <subtitle.srt>
```

Subtitles can be given as an optional second argument. If no subtitle argument is found, RaspberryCast will attempt to find a subtitle file with the same name as the video. In the case of TV shows and movies, RaspberryCast will attempt to match the video with an appropriate subtitle file. This behaviour can be disabled in the configuration file.

## Demos

Demo video with the Chrome extension:

[![Video 1](http://img.youtube.com/vi/0wEcYPSm_f8/0.jpg)](http://www.youtube.com/watch?v=0wEcYPSm_f8)

Demo video with an Android (also works on iOS):

[![Video 2](http://img.youtube.com/vi/ZafqI4ZtJkI/0.jpg)](http://www.youtube.com/watch?v=ZafqI4ZtJkI)

## Uninstall
Remove reference to RaspberryCast.sh in /etc/rc.local

Delete the /home/pi/RaspberryCast/ folder.

## Contribute

If you enjoyed using RaspberryCast, and/or would like to support the development, please consider making a donation.

## License
Code released under the MIT license. 

You are welcome to contribute to the project.

