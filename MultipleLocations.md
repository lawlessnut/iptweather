A nice new feature in IPTWeather: all favorite cities can be displayed at once with their own current weather icon!

Here's how to get this result:<br>
<img src='http://iptweather.googlecode.com/files/MultipleLocationsTito12.jpg' alt='' border='0' /><br>
<br>
1- IPTW doesn't create icons so you have to create new empty icons in your weather page (for me 20: 8 cities + 12 forecast icons). You might want to add 3 other icons at the bottom or anywhere convenient for you linked to <b>iPhoneTodayAccuWeather.mscr</b> (this is for update), <b>manageIPTWLocation.mscr</b> and <b>IPTWeatherConfig.mscr</b> (links to the two last scripts already in Start Menu -> IPTWeather).<br>
<br>
2- Edit weather.ini using <b>IPTWeatherConfig.mscr</b> this way:<br>
<b>IPTWcurrentWeatherIcon=0</b><br>
IPTWcurrentWeatherPage=0<br>
IPTWforecastStartIcon=8<br>
IPTWforecastStartPage=0<br>
IPTWcurrentWeatherIconTextPattern=%CITY%<br>
<br>
<font color='red'>If you want to have IPTW on a separate folder (<a href='http://forum.xda-developers.com/showpost.php?p=10953917&postcount=2686'>Folders for iPT</a>) then you set:</font><br>
<font color='red'>IPTWiPhoneTodayClassName=FolderW</font><br>
<br>
You can change the page (0 is the first one) and the icons location, but remember to leave enough room for the favorite cities so they will not overwrite the forecast icons.<br>
<br>
3- Click on <b>manageIPTWLocation.mscr</b>, double click "Favorites to show current weather of", double click all favorite cities you want - a + will appear next to the name, when finished press cancel to return to menu, double click "Favorites to auto-update", double click all favorite cities you want - a <code>*</code> will appear next to the name. When finished press cancel twice to exit.<br>
<br>
4- Make sure you have Internet or data connection active then press <b>iPhoneTodayAccuWeather.mscr</b> to update. Now you just have to press the location icon to get the forecast updated for this location!