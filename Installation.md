### Prerequesite: ###
  * **Install** <a href='http://forum.xda-developers.com/showthread.php?t=633618'>tronikos' iPhoneToday</a>**and/or**<a href='http://s2u2.ac-s2.com/'>S2U2</a><br />
  * **Install** <a href='http://www.sto-helit.de/downloads/mortscript/MortScript-4.2.zip'>Mortscript 4.2</a> or even <a href='http://www.sto-helit.de/forum/download/file.php?id=265'>MortScript 4.3b15</a>**for faster run**<br />
  * Optionnaly, to use the 'My Location' feature, install <a href='http://forum.xda-developers.com/showthread.php?t=607102'>Sleuth's myLocation Service</a><br />
  * **Install the latest IPTWeather** cab file provided <a href='http://code.google.com/p/iptweather/downloads/list'>here</a>. (the configuration at installation is the one I use with S2U2 and iPhoneToday with the current weather icon displayed in place of the top left icon on the first page)<br />
### **IMPORTANT**: ###
  * **Any question? Need some help? Please check the**<a href='http://code.google.com/p/iptweather/wiki/FAQ'>FAQ</a> first, then dicuss on the <a href='http://forum.xda-developers.com/showthread.php?t=603817'>xda thread</a>.<br />
  * **Configure all** settings listed below and others by running **'ITPWeather Config'** shortcut from the **Start Menu**. (or edit the <a href='http://code.google.com/p/iptweather/wiki/Configuration'>weather.ini file</a>)<br />
  * **Change** your weather **location** by running **'ITPWeather Location'** shortcut from the **Start Menu**. (or edit the <a href='http://code.google.com/p/iptweather/wiki/Configuration'>weather.ini file</a>)<br />
  * Please note that if you don't have S2U2 installed on your device, ITPWeather will automatically disable all features related to S2U2! The same for iPhoneToday!<br />
### Next installation steps: ###
  * **To use IPTWeather in iPhoneToday** (if you haven't installed iPhoneToday, IPTWeather will automatically disable all its features related to iPhoneToday):<br />
    * extract an icon set (<a href='http://iptweather.googlecode.com/files/accuweathericons.zip'>accuweathericons.zip</a> or <a href='http://iptweather.googlecode.com/files/spilicons.zip'>spilicons.zip</a> or from other users) to any folder and change **`IPTWaccuWeatherIconPath`** in the **`User settings`** to point to this folder.<br />
    * launch iPhoneToday, and configure/edit the first icon on the first page (or change **`IPTWcurrentWeatherIcon`** and **`IPTWcurrentWeatherPage`** in the **`User settings`**) by setting the 'Execute' field to call the script **iPhoneTodayAccuWeather.mscr**. This icon will show the current weather.<br />
  * **To use IPTWeather in S2U2 wallpaper** (if you haven't installed S2U2, IPTWeather will automatically disable all its features related to S2U2):<br />
    * extract <a href='http://iptweather.googlecode.com/files/AccuWeatherHD_20100420.zip'>AccuWeatherHD.zip</a> (or <a href='http://iptweather.googlecode.com/files/S2U2wallpaper_20100421.zip'>S2U2wallpapers.zip</a> or <a href='http://iptweather.googlecode.com/files/howdykeith_Accuw%20Lands%20icons_by_Michoob.zip'>howdykeith's Accuw Lands icons</a>) to any folder and change **`IPTWS2U2WallpaperPath`** in the **`S2U2 settings`** to point to this folder.<br />
  * **To use IPTWeather with S2U2 UserWeather** (bottom left weather icon in S2U2) (if you haven't installed S2U2, IPTWeather will automatically disable all its features related to S2U2):<br />
    * extract <a href='http://iptweather.googlecode.com/files/S2U2icons.zip'>S2U2icons.zip</a> (or <a href='http://iptweather.googlecode.com/files/S2U2spilicons.zip'>S2U2spilicons.zip</a>) into your **`\Program files\S2U2\gfx`** folder (or in another folder defined by **`IPTWS2U2UserWeatherIconsPath`** in the **`S2U2 settings`**).<br />
  * **Configure ITPWeather by running the 'IPTWeather Config' shortcut in the Start Menu** (or by editing the <a href='http://code.google.com/p/iptweather/wiki/Configuration'>weather.ini file</a>).<br />
  * **Run 'Start IPTWeather'** so the next update will be scheduled in **`IPTWdelayHours`** hours and **`IPTWdelayMinutes`** minutes (settings in the **`User settings`**).<br />
  * If you don't want to wait for the next scheduled update, you can:<br />
    * either run 'IPTWeather Location' from the Start Menu and choose your city so you get a pop-up to update the weather,<br />
    * or tap your new IPTWeather icon in iPhoneToday once to show weather forecasts, and a second time to get the dialog box to force the update,<br />
    * or just run the `getAccuWeather.mscr` script in the `sys` folder.<br />