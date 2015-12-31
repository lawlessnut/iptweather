### Prerequesite ###
  * **Install** <a href='http://forum.xda-developers.com/showthread.php?t=633618'>tronikos' iPhoneToday</a>**and/or**<a href='http://s2u2.ac-s2.com/'>S2U2</a><br />
  * **Install** <a href='http://www.sto-helit.de/index.php?module=download&amp;action=view&amp;entry=65'>Mortscript 4.2</a> or even <a href='http://www.sto-helit.de/forum/download/file.php?id=265'>MortScript 4.3b15</a>**for faster run**<br />

### Install ###

  * Download:<br />
    * the latest IPTWeather cab file provided <a href='http://code.google.com/p/iptweather/downloads/list'>here</a>.<br />
    * iconset <a href='http://iptweather.googlecode.com/files/spilicons.zip'>spilicons.zip</a> or <a href='http://iptweather.googlecode.com/files/accuweathericons.zip'>accuweathericons.zip</a>.<br />
  * Install the cab in device memory.<br />
  * Unzip the iconset and move the folder to `\Program Files\IPTWeather`<br />

### Configure basics ###

  * Launch IPhoneToday and configure the 1st icon on the 1st page (note that if you have something else than a blank icon you'll have to copy it first to another place). Long press on it, choose "Edit icon", in "Execute" field navigate to "\Program Files\IPTWeather\iPhoneTodayAccuWeather.mscr". You can leave "Image" empty, save and exit. <br />
  * Run **'IPTWeather Config'** from the Start Menu for configurations:<br />
    1. In the **`User settings`** change **`IPTWaccuWeatherIconPath`** if needed to point to the **`\Program Files\IPTWeather\spilicons`** folder.<br />
    1. **`IPTWhideNightForecastIcons`**: I set the value to 1 to remove night icons.<br />
    1. **`IPTWmondayText`**, **`IPTWtuesdayText`**, **`IPTWwednesdayText`**, etc.: change to your language, "Lu: " to "Mon: " etc.<br />
    1. **`IPTWcurrentWeatherIconTextPattern=%PT% (%PRFT%)`**: you can remove the function with the brackets to prevent long text overlapping<br />
    1. **`IPTWforecastWeatherIconsTextPattern=%SDAY%%PT% (%PRFT%)`**: same as above<br />
  * Run **'IPTWeather Location'** from the Start Menu, then choose or search for your location.<br />

### And see the result ###
Now you can reset your device, connect to Wifi and press your new IPTWeather icon.<br />
You should get now a weather icon with current temp and below 5 more days forecast.<br />
If everything is working you can return to configure IPTWeather with it endless possibilities by running **'IPTWeather Config'** from the Start Menu or by editing the weather.ini file.<br />