<b><font color='green'>Q: I want to test my IPTWeather settings. My update interval is set to 1 minute, but still it seems I cannot have IPTWeather updated with my new settings. I am out of idea...</font></b><br />
A: Normally, it is useless to have an update interval less than 30 minutes because AccuWeather.com does not update the data more often than every 30 minutes.
For testing purpose, I would also advise not to set the update interval to less than 2 or 3 minutes, because of the required time to set up an active connection, to download the data and to update iPhoneToday.
Because the risk is that while IPTWeather is updating, the next update is triggered by Windows Mobile, but as MortScript cannot run several times at once the same script, this next update will be just ignored by MortScript without scheduling any next update, and the consequence will be that IPTWeather will stop auto-updating...
But to test your settings, no need to have a small update interval.
**The best and easiest way to test your settings is just to run the 'IPTWeather Location' script and select again the current location (better save it into your favorites from the 'IPTWeather Location' script).**<br />
<br />
<b><font color='green'>Q: I want to create shortcut in my theme (HS++) when clicked it "Manually" update the weather for all cities "or to last city selected" listed to the registry ... Is it possible?</font></b><br />
A: To manually update the weather, the best is to run the iPhoneTodayAccuWeather.mscr script, even if you don't use iPhoneToday but only S2U2.
Then, if the last update time is longer ago than IPTWforceDelayHours + IPTWforceDelayMinutes, it will update all the locations set to be auto-updated via the 'IPTWeather Location' script (see in the Start menu).
With the iPhoneTodayAccuWeather.mscr script, you can also update only one location if you call it with parameter IPTWaccuWeatherLocationForecast="the location AccuWeather code" and IPTWFIP=0 (position of the icon in iPhoneToday - mandatory, even if you don't use iPhoneToday).<br />
<br />
If you don't care about IPTWforceDelayHours + Minutes, and want to force the update as soon as you click on your shortcut, then call the getAccuWeather.mscr script with the same settings described above than for iPhoneTodayAccuWeather.mscr.<br />
<br />
<b><font color='Green'>Q: How to replace strange symbols by good ones:<br>
Ã± by ñ, Ã¡ by á, Ã³ by ó, Ã by í, íº by ú, í‘ by Ñ, Ãº by ú, í© by é?</font></b><br />
A: In the sys folder, edit the ini file of your language and set the following first line (see fr.ini for an example):<br />
ReplaceMap=Ã±,ñ,Ã¡,á,Ã³,ó,Ã,í,íº,ú,í‘,Ñ,Ãº,ú,í©,é<br />
<br />
<b><font color='Green'>Q: How to display all favorite cities at once with their own current weather icon in iPhoneToday?</font></b><br />
A: <a href='http://code.google.com/p/iptweather/wiki/MultipleLocations?ts=1298879149&updated=MultipleLocations'>follow tito12's tutorial</a><br />
<br />
<b><font color='Green'>Q: I cannot display a specific icon for a location as the city icon for a location code with a + in it. For instance, for the location code MEA|IL|IS005|TEL+AVIV, if I set an icon named 'MEA_IL_IS005_TEL+AVIV.png', it is not displayed, but the IPTWdefaultCityIcon is displayed instead.</font></b><br />
A: You actually must replace the + by a blank space for the icon name and it will work. For the above example, just set the icon name to 'MEA\_IL\_IS005\_TEL AVIV.png'.<br />
<br />
<b><font color='Green'>Q: I've tried all but it doesn't download anything even if I have an active connection. The data.xml file in the sys folder is not updating.</font></b><br />
A: You may be using the MortScript which is cooked into your ROM. Then try to reinstall MortScript (either <a href='http://www.sto-helit.de/index.php?module=download&amp;action=view&amp;entry=65'>MortScript 4.2</a> or <a href='http://www.sto-helit.de/forum/download/file.php?id=265'>MortScript 4.3b15</a>).<br />
<br />
<b><font color='Green'>Q: I'm getting constant Mortscript errors when it tries to update ("A problem has occurred with MortScript.exe").</font></b><br />
A: MortScript cannot toggle the data connection off on some ROMs and just crashes.<br />
You can bypass this by installing <a href='http://www.vijay555.com/?Releases:VJVolubilis'>VJVolubilis</a> and setting IPTWinternetConnection=VJVolubilis. Depending on your OS language, you might have to change IPTWvjvolubilisPath.<br />
For your information, VJVolubilis is an app to toggle your data connection, and it works better than MortScript to achieve that.<br />
<br />
<b><font color='Green'>Q: I want to install the latest version of IPTWeather, but I'm scared to install it because I don't want to loose all my so hardly configured settings in the weather.ini file.</font></b><br />
A: You can update to the newest IPTWeather version without being scared of loosing all your settings:<br />
1 - backup your weather.ini by creating a copy of it anywhere.<br />
2 - install latest version of IPTWeather (Killing Dragon or upper)<br />
3 - run the new script restoreConfigBackup.mscr<br />
4 - select your backup weather.ini<br />
5 - and your settings are restored!<br />
<br />
<b><font color='Green'>Q: IPTweather have some bug, it can update weather only several time after install, after this can't update at any time.</font></b><br />
A: ~~Try restarting your device. It may happen sometimes that the MortScript is "locked" during the download process, thus resulting in not updating any more. I cannot do anything about that. It is a MortScript limitation.~~<br />
This is actually a bug in refreshing S2U2! I managed to bypass this. It fixed since the version 20101119.<br />
<br />
<b><font color='Green'>Q: Could IPTWeather display in iPhoneToday a humidity icon?</font></b><br />
A: Yes, IPTWeather can do that thanks to the userScriptOnUpdate.mscr script wich allows the user to have some custom features. Please check the following link for [full instructions on how to add this feature](http://forum.xda-developers.com/showpost.php?p=6905046&postcount=523) (included in latest versions of IPTWeather).<br />
<br />
<b><font color='Green'>Q: I use IPTWeather My Location service or Google Latitude to retrieve the location for current weather, but it doesn't seem very accurate because it gives me the weather of a city like 30 km from my location, even if Google Maps can find my position about 500 meters from my current. What could be the problem?</font></b><br />
A: AccuWeather's database to translate GPS position into a city is not very accurate (precision around 30km). You cannot do anything but find the exact code of your location using the script manageIPTWLocation.mscr.<br />
<br />
<b><font color='Green'>Q: I have configured the weather.ini file to display weather icons in iPhoneToday on a place where there is no icon. Nothing is displayed.</font></b><br />
A: If you want to have specific icons just for the weather and nothing else, you need to create blank icons in iPhoneToday. Because of the design of iPhoneToday, IPTWeather cannot create icons, but only update icons. The same rule applies if you want to have a page dedicated to weather icons.<br />
<br />
<b><font color='Green'>Q: I have french (or something) shortnames for the days of the week. Jeu, Ven, Dim, etc.</font></b><br />
A: In your weather.ini file, change the settings IPTWmondayText, IPTWtuesdayText, ..., IPTWsundayText.<br />
<br />
<b><font color='Green'>Q: I have moved the weather icon in iPhoneToday, but IPTWeather keeps updating the previous icon and not the new one!</font></b><br />
A: IPTWeather updates with the current weather the icon defined in the weather.ini file by the settings IPTWcurrentWeatherIcon and IPTWcurrentWeatherPage.<br />
<br />
<b><font color='Green'>Q: What is the iPhoneTodayAccuWeather.mscr script for?</font></b><br />
A: This script expands, without modifying your icons.xml file, all weather forecast icons in iPhoneToday at first call. If you call it a second time, weather forecast icons are hidden and it's back to your icons.xml configuration.<br />
If you actually want to write the weather forecast icons into your icons.xml configuration, just set IPTWwriteForecastInFile=1.<br />
<br />
<b><font color='Green'>Q: How to easily change the weather location?</font></b><br />
A: Call the manageIPTWLocation.mscr script. You can also set your favorite locations thanks to this script.<br />
<br />
<b><font color='Green'>Q: What is the quickIPTWFavoriteLocationChange.mscr script for?</font></b><br />
A: This script allows you to change your current location to your next favorite location. You can set your favorite locations by calling the manageIPTWLocation.mscr script.<br />
<br />
<b><font color='Green'>Q: What is the setIPTFavoriteLocation.mscr script for?</font></b><br />
A: This script allows you to change your current location to the favorite location of your choice. By default, it changes your location to your fifth favorite location. You may want to make copies of this script and edit each copy, to have for instance setIPTFavoriteLocation0.mscr, setIPTFavoriteLocation1.mscr, etc., each one allowing you to change your current location directly to your first, second, etc., favorite location.<br />
<br />
<b><font color='Green'>Q: What is the startAccuWeather.mscr script for?</font></b><br />
A: This script is to actually start IPTWeather. When you install the cab, a shortcut to this script is created to call this script.<br />
<br />
<b><font color='Green'>Q: What is the autostartIPTWeather.mscr script<br>
for?</font></b><br />
A: This script creates a shortcut to the startAccuWeather.mscr script in your Windows StartUp menu, to start IPTWeather when you restart your device. This script should only be used if you want to change the installation directory of IPTWeather.<br />
<br />
<b><font color='Green'>Q: How to use IPTWeather only with S2U2, not with iPhoneToday?</font></b><br />
A: In the weather.ini file, set IPTWiPhoneTodayDisabled=1.<br />
Please note it will be automatically disabled if iPhoneToday is not running nor installed, unless IPTWiPhoneTodayDisabled=-1.<br />
<br />
<b><font color='Green'>Q: How to use IPTWeather only with iPhoneToday, not with S2U2?</font></b><br />
A: In the weather.ini file, set IPTWtomorrowForecastInS2U2UserWeather=0, IPTWtodayForecastInS2U2Wallpaper=0, and IPTWtodayForecastInS2U2Text=0.<br />
Please note it will be automatically disable if you have not installed S2U2 on your device.<br />
<br />
<b><font color='Green'>Q: The text shown on the S2U2 slider is sometimes to long and is not entirely visible and the right margin is out of the text box. Can I fix it somehow?</font></b><br />
A: In the weather.ini you can set the IPTWlanguageFile to the weather description file you want. By default, it is eng.ini but you can change it. You can also change the text to fit your language or the size you want.<br />
<br />
<b><font color='Green'>Q: I'd like the text shown on the S2U2 slider to be in a different language. Is it possible?</font></b><br />
A: Change the setting IPTWtranslationLanguageCode to fit your language. Default language is US English.<br />
You can also edit manually the weather description file which is the file set in IPTWlanguageFile to change or force the weather descriptions. By default, it is set to the eng.ini file which located in the sys folder of IPTWeather.<br />
<br />
<b><font color='Green'>Q: How to change the installation path?</font></b><br />
A: To change the installation path of the IPTWeather folder, you have to:<br />
0 - Move the IPTWeather to the folder you want and check the path of your icons in the weather.ini file<br />
1 - Run the autostartIPTWeather.mscr script<br />
2 - Run the startAccuWeather.mscr script<br />