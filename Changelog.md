### ITPWeather\_20110910 ###
  * Corrected iPhoneToday icon shifting when sun has set and before midnight.
  * Corrected bug that manage location might not be able to connect or detect active connection.
  * Added option IPTWuseS2U2wallpaperForBackground = -1 to show current weather in iPhoneToday wallpaper.

### IPTWeather\_20110621 ###
  * added iPhoneToday setting IPTWmaxForecastDaysToShow to limit the number of days of weather forecast icons shown in iPhoneToday (to limit to 4 days even if 8 days are downloaded for instance…).
  * added iPhoneToday setting IPTWforecastDaysToSkip to set a number of days of weather forecast icons to skip in iPhoneToday (not to show current day forecast for instance…).
  * added many shortcuts in the Start Menu/IPTWeather folder.
  * now, when IPTWwriteForecastInFile=1, setting IPTWforecastIconSkipFirstAtSunset=0 works.
  * small performance optimization when IPTWhideNightForecastIcons=1.

### IPTWeather\_20110511 ###
  * added the "header:" prefix for the IPTWforecastStartPage setting so you can set the page header name instead of the page number (very usefull if you which to move your iPhoneToday weather page around...)
  * now working weather background for iPhoneTodayDesktop.exe
  * code improvement (use of += 1 instead of = ... + 1, less duplicated code, added some tests)
  * corrected bug that the goToAccuWeather question was displaying empty dialog box.
  * corrected bug that the error icon was not displayed in iPhoneToday on current weather icon when there were update errors (rather rare...)
  * optimized check for live connection
  * updated to iniEditor\_v05

### IPTWeather\_20110330 ###
  * corrected bug: now you can display the days of week even if language is not US-English.
  * corrected bug: wrong time comparisons when in daylight saving time.
  * back IPTWwriteForecastInFile=0 by default.
  * better power management change triggering.
  * added 'RIL Map' connection type for setting IPTWinternetConnection.
  * now IPTWinternetConnection can be a list of connection types, comma separated. IPTWeather will try each one of them until it connects successfully.
  * now choosing a location from the manageIPTWLocation.mscr script only updates this one and not all starred ones at script exit.
  * added Spanish weather description language file.
  * added mapping for k/h to km/h in the French lang.ini file.
  * added Spanish lang.ini language file.
  * better ReplaceMap and AutoTextShortening for the fr.ini file.

### ITPWeather\_20110303 ###
  * new setting IPTWobservationTimeExecField to run any script or app when clicking on the weather update time icon in iPhoneToday.
  * split [settings](User.md) into [settings](General.md) and [settings](iPhoneToday.md): make sure to run the restoreBackupConfig.mscr script to restore your backup weather.ini file!
  * added the %SCITY% text pattern for cities short names defined in the citiesShortNames.ini file.
  * do not display any dialog box while running the quickIPTWFavoriteLocationChange.mscr script if IPTWupdateWeatherNowQuestion is empty.
  * IPTWiPhoneTodayClassName setting also used in the 'IPTWeather Location' script.
  * the IPTWupdateWeatherNowQuestion dialog box title contains ' + ...' when all the favorite locations with `*` are to be updated.
  * corrected bug that current weather icon of favorite locations with a + was not display if no location had a `*`.
  * Added Wifi option for the IPTWinternetConnection setting.

### IPTWeather\_20110213 ###
  * Removed all comments from weather.ini file for better performance of IPTWeather. All comments are now in the weather.ini.desc description file that is used for the IPTWeather Config script.

### IPTWeather\_20110212 ###
  * Actually fixed display if IPTWeather update time is after sunrise/sunset but AccuWeather observation time is before.
  * Added feature to update the weather data for all starred favorite locations (see IPTWeather Location script).
  * Display of current weather icons for selected favorite locations in iPhoneToday (see IPTWeather Location script).
  * Added IPTWiPhoneTodayClassName setting to allow the use of any iPhoneToday instance (Tito's iFolder and so on).
  * IPTWtranslationLanguageCode setting back with language codes de, es, fr, it and pt (empty by default for US-English).
  * Added ReplaceMap setting in the weather description .ini files (see eng.ini and fr.ini for examples).
  * Added AutoTextShortening setting in the weather description .ini files (see eng.ini and fr.ini for examples).
  * Added %TUNIT% and %SUNIT% patterns for Temperature and Speed units.
  * Add VJVolubilis support to the Manage Location script.
  * Totally reviewed IPTWeather Location script for more user-friendlyness.
  * Blank unused weather icons in iPhoneToday if IPTWwriteForecastInFile=1.
  * Use WindowsProcess instead of ProcExists to detect iLock2.exe is stopped (S2U2).
  * Code optimization.

### IPTWeather\_20101215 ###
  * Fixed display if IPTWeather update time is after sunrise/sunset but AccuWeather observation time is before.
  * Small code improvement.

### IPTWeather\_20101202 ###
  * At installation, create the 'Start IPTWeather' shortcut in the StartUp folder.
  * If IPTWwriteForecastInFile=1, then automatically display forecast icons in iPhoneToday.
  * To avoid issues with S2U2, removed use of the Kill function of MortScript and run iLock2.exe -slide instead of s2u2.exe.
  * Check S2U2 icon file sizes to ensure UserWeather icons are updated correctly if IPTWS2U2UserWeatherIconsPath is changed and/or if icons are changed within the same folder.
  * Removed not well working IPTWmaxDownloadMinutes setting.
  * If S2U2 not installed, disable S2U2 related features before updating S2U2 registry.
  * Disabled IPTWtranslationLanguageCode setting which cannot work since last AccuWeather.com website update.
  * IPTWalsoDisplayOriginalDescInIPT=0 by default.

### IPTWeather\_20101119 ###
  * Better management of weather update download kill system (data refreshed even after an update failure).
  * Corrected major bug that IPTWeather may be blocked if S2U2 fails to be restarted correctly (S2U2 issue).
  * Corrected bug in observation dates (introduced in previous version).
  * Corrected bug in obsolete data display (introduced in previous version).
  * Small code improvements.

### IPTWeather WWI (aKa IPTWeather\_20101111) ###
  * Code refactored for less duplicated code.
  * Enhanced connection management in the change location script.
  * Added setting IPTWmaxDownloadMinutes to kill the update after some time to avoid strange behaviour if the update fails but locks MortScript.
  * Now, if last update has been done before the sunrise (or sunset), and time is after the sunrise (or sunset), data are considered as obsolete.
  * Change rdona API by ruan API by default.
  * Now, can load AccuWeather forecasts from 1 to 7 forecast days instead of fixed 5, depending on the number of days available in the API.
  * Corrected bug that the wrong weather information may be showed during night before the sunrise if data are not up-to-date.
  * Do not reload S2U2 wallpaper if pictures cannot be found, for instance if pictures are on the storage card and the device is connected to a PC.
  * Corrected bug on winter time management.

### IPTWeather Killing Dragon (aKa IPTWeather\_20100929) ###
  * New script IPTWeatherConfig.mscr to help configuring IPTWeather and the weather.ini file.
  * More generic IPTWreloadIcon.mscr script to allow full customization of icon texts in iPhoneToday.
  * IPTWeather doesn't remove any notification anymore if IPTWdelayHours=0 and IPTWdelayMinutes=0. Usefull to use an external notification system.
  * Removed setting IPTWS2U2Path.
  * Removed setting IPTWhideRealFeelInForecastIcons (configure IPTWforecastWeatherIconsTextPattern instead).
  * Removed setting IPTWquickLocationChangeSleepMsgTime (status message instead).
  * Replaced IPTWS2U2iconText.mscr script by more generic IPTWtextPattern.mscr script.
  * Added setting IPTWhideNightForecastIcons.
  * Added settings IPTWcurrentWeatherIconTextPattern and IPTWforecastWeatherIconsTextPattern to customize icon texts in iPhoneToday.
  * Added symbols %DAY%, %SDAY%, %PT% and %PRFT% for the three <...>TextPattern settings (check weather.ini file comments for more help).
  * Added settings IPTWS2U2WallpaperLPath and IPTWdefautS2U2WallpaperL for landscape wallpaper in S2U2.
  * Reviewed comments in the weather.ini file for better understanding of the different settings.
  * Corrected bug when no data was available that IPTWdefaultS2U2Text was not displayed in S2U2 and IPTWtodayForecastInS2U2Text was set to 0.
  * Added city and state in the title of the dialog box asking for updates.

### IPTWeather\_20100826 ###
  * If no weather translation found, then use default non-translated language.
  * Added IPTWS2U2UserWeatherIconsPath setting to use any path for S2U2 weather icons (by default, old behaviour by using icons in the S2U2\gfx\weather folder).
  * Added IPTWalsoDisplayOriginalDescInIPT option to display non-translated weather description in the iPhoneToday pop-ups.
  * Weather translation compatible with the new AccuWeather site coding.
  * Compatible with the iPhoneTodayDesktop.exe version.
  * Removed IPTWdisconnect.mscr script for better disconnection management.
  * Keep forecast weather icons expanded in iPhoneToday after changing location.
  * Now, by default, IPTWtranslationLanguageCode is empty so there is no weather description translation.
  * Added lang\_fr.ini fo French lang.ini file to rename to lang.ini to have French text in iPhoneToday.

### IPTWeather\_20100712 ###
  * Added parameter IPTWhideRealFeelInForecastIcons to set to 1 no to show Real Feel temperatures in weather forecast icons in iPhoneToday.
  * Added parameter IPTWwriteForecastInFile to set to 1 to write icons in the icons.xml file of iPhoneToday.

### IPTWeather\_20100711 ###
  * Working multi-language weather description even if IPTWtodayForecastInS2U2Text=0.
  * Added multi-language for %TXT% in IPTWS2U2UserWeatherTextPattern.

### IPTWeather\_20100709 ###
  * SystemPath used to display the weather data when forecast icons are shown in iPhoneToday.
  * unitSpeed and unitTemp can now be translated in the lang.ini file.

### IPTWeather\_20100708 ###
  * Now, when you click on a forecast icon in iPhoneToday, you get more weather information (only compatible with iPhoneToday 1.5.3 and up). You can customize the displayed language in the lang.ini file.
  * Added humidity icon.
  * Added unitTemp and unitSpeed.
  * Added option IPTWtranslationLanguageCode to have an automatic multi-language support (uses 10 times more data than default without translation).
  * Added option IPTWconvertTimeFormat to convert sunrise and sunset time to the 24 hours format.

### IPTWeather\_20100528 ###
  * IPTWforecastSkipIconFrequency counts the empty icon left after sun has set when using IPTWforecastIconSkipFirstAtSunset=1.
  * IPTWforecastIconSkipFirstAtSunset set to null by default in the weather.ini file.

### IPTWeather\_20100527 ###
  * Added setting IPTWforecastIconSkipFirstAtSunset to be set to 1 in order to have a one icon shift when showing the weather forecast icons in the evening (when sun has set).

### IPTWeather\_20100526 ###
  * Added setting IPTWvjvolubilisPath with the option VJVolubilis for the IPTWinternetConnection setting to use VJVolubilis to toggle the data connection for devices that don't support MortScript connection toggling (download VJVolubilis at http://www.vijay555.com/?Releases:VJVolubilis).
  * Added settings IPTWforecastSkipIconFrequency and IPTWforecastSkipIconQuantity to configure some blank icons every some weather forecast icons in iPhoneToday.
  * Added script stopAutoUpdate.mscr to remove and disable any automatic update.

### IPTWeather\_20100510 ###
  * Working IPTWiPhoneTodayDisabled=-1 feature

### IPTWeather\_20100509 ###
  * Option IPTWiPhoneTodayDisabled=-1 working as expected (check weather.ini file for more information)
  * Update iPhoneToday weather icons even if weather forecast icons are displayed, so you can have a page dedicated to weather forecasts without having to expand/collapse weather forecast icons

### IPTWeather\_20100429 ###
  * Bypass an issue in iPhoneToday so you can keep your original icons.xml file safe. The issue is that if you have some temp icons defined with the reloadIcon=1 feature (weather forecast icons), then, if you set an icon with reloadIcon=2 to write this and only this icon in the icons.xml file (current weather icon), all the temp icons will also be written in the icons.xml file and not only the icon defined with reloadIcon=2

### IPTWeather\_20100428 ###
  * Added option IPTWiPhoneTodayDisabled=-1 if you don't want that IPTWeather disables automatically iPhoneToday IPTWeather features
  * Data update time is compared in device time so displayed data are alright even when weather data are from another time zone
  * If IPTWupdateWeatherNowQuestion was empty, then iPhoneTodayAccuWeather.mscr was always updating data when hiding weather forecasts, and not only if data were older than IPTWforceDelayHours and IPTWforceDelayMinutes
  * Cleaned code

### IPTWeather\_20100425 ###
  * Automatically set UserWeather to 05 in S2U2 settings if IPTWtomorrowForecastInS2U2UserWeather = 1 or IPTWtomorrowForecastInS2U2UserWeather = -1
  * Shortcut created in overwrite mode when running the autostartIPTWeather.mscr script
  * Added option IPTWreloadLastDataOnStart=-1 (by default) so IPTWeather doesn't reload data at device start, since it is no longer needed with latest tronikos' iPhoneToday versions thanks to the reloadIcons=2 feature. And this bypass iPhoneToday 1.5.1 and 1.5.2 issue with the managing of the registry values at start
  * Added waitForReadyIPT.mscr script for better code maintenance
  * Added a timer for iPhoneToday registry updates so IPTWeather doesn't enter in an infinite loop if there is a bug with iPhoneToday

### IPTWeather\_20100423 ###
  * Automatically disable iPhoneToday's IPTWeather icon updates if it is not used.
  * Bypass an issue of iPhoneToday in version 1.5.2, that do not reset the registry value reloadIcons on start.

### IPTWeather\_20100422 ###

  * No question for update when changing location if IPTWupdateWeatherNowQuestion is empty.
  * Added setting IPTWS2U2UserWeatherIconToForce
  * Added setting options IPTWtodayForecastInS2U2Wallpaper=-1 and IPTWtodayForecastInS2U2Text=-1 to show the current weather in the S2U2 wallpaper and/or S2U2 slide text.
  * Changed the default installed weather.ini file so the S2U2 wallpaper is the HD one.

### IPTWeather\_20100418 ###

  * Correct config.xml file.

### IPTWeather\_20100417 ###

  * Known issue: error on update because of a bad config.xml file.
  * Added fields %WSPD%, %WDIR% and %WGUS% for the IPTWS2U2UserWeatherTextPattern setting to display the wind speed, direction and gusts.
  * Added shortcut 'IPTWeather Location' to the manageIPTWLocation.mscr script in the Start Menu\Programs\IPTWeather folder.

### IPTWeather\_20100415 ###

  * IPTWeather can now be installed in any directory, so it is by default installed in the \Program Files\ directory.
  * Installation cab for scripts. You still have to configure manually the weather.ini file and to download icon/wallpaper sets.

### IPTWeather\_20100414 ###

  * Code optimizations.
  * Added %HUM% for the IPTWS2U2UserWeatherTextPattern setting to show current humidity.
  * Corrected wrong current location display in the manageIPTWLocation.mscr script.
  * Decreased sleep time for faster icon updates in iPhoneToday.
  * Added ShowWaitCursor when runnin the iPhoneTodayAccuWeather.mscr script.
  * New userScriptOnUpdate.mscr script. It's a kind of API run at each display update where you can call your own custom scripts (to play a sound on weather updates, etc.).
  * Project moved onto Google Code.
  * Added Modaco App-to-date support.

### IPTWeather\_20100401 ###

  * If IPTWgoToAccuWeatherQuestion is empty, the weather update will be forced without a question.
  * Added field %TXT% for the IPTWS2U2UserWeatherTextPattern setting to display the weather description.
  * If it is past midnight, and no new data is available, then, with IPTWtomorrowForecastInS2U2UserWeather=-1, not last current weather icon/text is displayed in S2U2 UserWeather, but current night icon/text and the obsolete data pattern applies.

### IPTWeather\_20100330b (47 downloads in xda) ###

  * Added following fields for the IPTWS2U2UserWeatherTextPattern setting: %CITY%, %SUNS%, %SUNR%, %OBSD% and %OBST%. Please check the weather.ini file for the description of each field.

### IPTWeather\_20100330 (2 downloads in xda) ###

  * By setting IPTWtomorrowForecastInS2U2UserWeather=-1, you'll have in S2U2 the current conditions icon, and under the icon, current temperatures
  * Added setting IPTWS2U2UserWeatherTextPattern to set the text pattern of the text displayed under the S2U2 User Weather icon. Please read the weather.ini file for further information. By default, it is set to display information related to IPTWtomorrowForecastInS2U2UserWeather=-1.

### IPTWeather\_20100328 (52 downloads in xda) ###

  * Check existence of S2U2 when IPTWtomorrowForecastInS2U2UserWeather=0 or IPTWtodayForecastInS2U2Wallpaper=0 or IPTWtodayForecastInS2U2Text=0 to avoid errors due to bad weather.ini file user configuration
  * Move non-user scripts used by IPTWeather to the sys folder
  * Simplified the "change IPTWeather installation path" procedure by removing the step "2 - change the path of the IPTWeather folder in the 3rd line of the config.xml file", and by replacing the step "1 - change the path of the IPTWeather folder in the 1st line of the startAccuWeather.mscr script" by "1 - Run the autostartIPTWeather.mscr script"

### IPTWeather\_20100325 (49 downloads in xda) ###

  * Corrected the automatic iPhoneToday path detection to make it work for each ROM language.

### IPTWeather\_20100323 (49 downloads in xda) ###

  * Added parameter IPTWaccuWeatherAPI set to rdona by default, in case AccuWeather disconnects the rdona API as the rainmeter API...
  * Detection of the use of the exe or the dll version of iPhoneToday is now based on the following registry value and not the existence of the iPhoneToday window: HKLM\Software\Microsoft\Today\Items\iPhoneToday\Enabled
  * If IPTWquickLocationChangeSleepMsgTime is not set, then the quickIPTWFavoriteLocationChange.mscr script sets it by default to 1
  * Removed setting IPTWiPhoneTodayPath: the path of iPhoneToday is automatically detected, so IPTWeather is compatible with all versions of iPhoneToday without having to change any setting :)

### IPTWeather\_20100322 (29 downloads on xda) ###

  * Removed setting IPTWuseExeIPhoneToday: now IPTWeather detects if you're using the exe or the dll version by its own.
  * 'My Location' location code doesn't use the IP address to define current location anymore, but Sleuth's myLocation Service
  * Added a test to avoid the error "'\Program Files\S2U2\lang.ini' couldn't be opened" when the user has badly configured IPTWeather
  * Added weather.ini file setting IPTWquickLocationChangeSleepMsgTime to set the number of seconds the message showing the new location has to be displayed for, when using the scripts quickFavoriteLocationChange.mscr and setIPTWFavoriteLocation.mscr
  * Optimization for iPhoneToday 1.5.0 and upper, but still compatible with the 1.3 version: use of the reloadIcon = 2 feature in order to update the icons.xml file for the main weather icon

### IPTWeather\_20100316 (209 downloads on xda) ###

  * Use of Rdona API to retrieve AccuWeather data :)
  * Changed script quickIPTWFavoriteLocationChange.mscr to jump to a specific favorite location when called with a parameter from another script. The parameter is the position of the location in the favorite list: if you have for instance three favorite locations, then the parameter may be 1, 2 or 3. If called without any parameter quickIPTWFavoriteLocationChange.mscr will behave as in the previous version, that means it will circle through favorite locations.
  * Added an example script setIPTFavoriteLocation.mscr that calls quickIPTWFavoriteLocationChange.mscr with the parameter 5, to jump directly to the fifth favorite location. You can map an iPhoneToday icon to call setIPTFavoriteLocation.mscr to change current weather to the fifth favorite location. You may want to make copies of this script, to have for instance setIPTFavoriteLocation0.mscr, setIPTFavoriteLocation1.mscr, etc.
  * Corrected issue: when no data at all was available, then IPTWeather could freeze, forcing to restart the phone and to delete some registry keys specific to iPhoneToday...

### IPTWeather\_20100304 (95 downloads on xda) ###

  * Known issue: doesn't work since Rainmeter API has been deprecated by AccuWeather :(
  * Changed default installation path to \IPTWeather instead of \iPhoneToday\IPTWeather
  * IPTWiPhoneTodayPath to set the iPhoneToday.exe and settings.xml path for 1.4x compatibility.
  * IPTWaccuWeatherIconPath to set the path for weather icons, to easily change your weather icon theme.
  * New spil icons theme.
  * Added a check on the data.xml file to avoid parsing pop-up errors.
  * Compatibility with iPhoneToday 1.4.3 and upper (just change the IPTWiPhoneTodayPath).
  * Not forcing background to be static when using IPTWuseS2U2wallpaperForBackground=1
  * Change of the location through the manageIPTWLocation.mscr script restore previousely downloaded data WITHOUT a new update.
  * New script quickIPTWFavoriteLocationChange.mscr to change current weather with just a single tap!
  * Added IPTWlocationLatitude and IPTWlocationLongitude to use your geographic location instead of an AccuWeather code, if IPTWaccuWeatherLocation is set to blank.
  * Corrected minor issue: when changing the location for a different time zone, the weather update may not be triggered correctly.
  * Corrected minor issue: no icon was drawn if there was no downloaded data.

### IPTWeather\_20100125 (158 downloads on xda) ###

  * Removed duplicated code sections by creating "sub" scripts => easier code maintenance + faster scripts!
  * New setting IPTWlanguageFile in the weather.ini file: put in the name of an ini file containing the "Weather description translation" section. You'll have to cut and paste the old "Weather description translation" section from the weather.ini to this new ini file, so the weather.ini file is smaller and the scripts get faster. By default, you have IPTWlanguageFile=eng.ini. Thanks to this, you can easily set different languages displayed in the S2U2 slide text, especially if different users share their language file ;)

### IPTWeather\_20100112 ###

  * Corrected issue: parsing error in the manageIPTWLocation.mscr script with some cities as Leicester. You have to enter the location code manually in the weather.ini...
  * Added Google Latitude setting in the manageIPTWLocation.mscr script
  * Added setting IPTWgoogleUserID (find your Google User ID here)
  * Added IPTWaccuWeatherLocation=Google Latitude option (also in the manageIPTWLocation.mscr script) in order to use your Google Latitude location as the weather location. Make sure to enable your Google Location Badge: http://www.google.com/latitude/apps/badge
  * Improved text shortening in the S2U2 slide text: "morning" replaced by "a.m.", "afternoon" replace by "p.m.", " ing" replaced by " in'"
  * Added setting IPTWiPhoneTodayDisabled: set it to 1 if you want to use S2U2 only

### IPTWeather\_20100108 ###

  * Uncommented first line of the getAccuWeather.mscr script (ErrorLevel("off")) to allow automatic recovery from download errors, as usual. I just forgot to do this in the previous version, sorry...
  * Kown issue: parsing error in the manageIPTWLocation.mscr script with some cities as Leicester. You have to enter the location code manually in the weather.ini...

### IPTWeather\_20100107 ###

  * If IPTWaccuWeatherLocation=My Location, then your location, based on IP geolocation, will be used to retrieve the weather forecast
  * Added the "My Location" option in the manageIPTWLocation.mscr script
  * Corrected minor bug: notifications are not correctly managed, so when forcing an update, you may get more automatic updates than expected for few updates...
  * Corrected display bug when using US zip codes as location codes and calling iPhoneTodayAccuWeather.mscr
  * No longer IPTWaccuWeatherLocationCode is used for the displayed city icon, but the location code stored in the registry after received data are parsed. Thus, even when using IPTWaccuWeatherLocation=My Location, you can still display the city icon (would be fun if we could have a city icon database...).
  * Corrected bug: "unknown command if" error in the startAccuWeather.mscr script
  * Better management of the IPTWpreventSleepModeOnUpdate setting when an error occurs during the update
  * Improved generation of new entries in the weather.ini file in the "Weather description translation" section: if the text is too long, " and " is replaced by " & ", and " with " is replaced by " w/ ". If you have other ideas on shortening the text...
  * Separated accuweathericons folder from the IPTWeather zip file so it is easier for you to update, especially if you use other icons.

### IPTWeather\_20100104 ###

  * Known minor bug: notifications are not correctly managed, so when forcing an update, you may get more automatic updates than expected for few updates...
  * Known bug: "unknown command if" error in the startAccuWeather.mscr script
  * New script manageIPTWLocation.mscr to easily change the weather location without the need of searching manually for an AccuWeather.com location code, and to manage a favorite locations list
  * New setting IPTWaccuWeatherFavoriteLocations
  * If IPTWdelayHours=0 and IPTWdelayMinutes=0, then no automatic update will be scheduled (perhaps it already worked, but now it's sure)
  * Replaced setting IPTWcityIcon with IPTWdefaultCityIcon: if an icon named "IPTWaccuWeatherLocationCode (with | replaced by underscores)"."IPTWiconsExtension" exists in the accuweathericons folder, then it will be used as the city icon to display, else the IPTWdefaultCityIcon will be displayed. For instance, if IPTWaccuWeatherLocationCode=EUR|FR|FR012|PARIS and IPTWiconsExtension=bmp, then the EUR\_FR\_FR012\_PARIS.bmp icon will be displayed if it exists.
  * Corrected the 18.jpg icon in the S2U2wallpapers pack => S2U2wallpapers\_20100104.zip

### IPTWeather\_20091229b ###

  * Added IPTWuseExeIPhoneToday=1 to make work the IPTWuseS2U2wallpaperForBackground setting even with the exe version of iPhoneToday

### IPTWeather\_20091229 ###

  * At last working and deeply tested the new feature IPTWuseS2U2wallpaperForBackground

### IPTWeather\_20091228d ###

  * Corrected section of the IPTWuseS2U2wallpaperForBackground. It is in the [settings](User.md) section of the weather.ini file, but in the 20091228c version, the script was not reading the parametter in the right section...
  * Known bug: IPTWuseS2U2wallpaperForBackground still doesn't work, especially not if you hadn't any wallpaper previousely defined in iPhoneToday

### IPTWeather\_20091228c ###

  * Added setting IPTWuseS2U2wallpaperForBackground to have the wallpaper changing in iPhoneToday as in S2U2
  * Known bug: new setting IPTWuseS2U2wallpaperForBackground doesn't work

### IPTWeather\_20091228b ###

  * Corrected S2U2 wallpaper forecast (when sun has not yet risen up, not current day forecast was shown, but the next night forecast...)

### IPTWeather\_20091228 ###

  * Corrected S2U2 wallpaper forecast (when sun has set, not current night forecast was shown, but the next night forecast...)

### IPTWeather\_20091227 ###

  * Some recode
  * Removed IPTWofflineMode weather.ini setting
  * Added 13 new optional User settings in the weather.ini file: IPTWobsoleteDataPrefix, IPTWupdateWeatherNowQuestion, IPTWforceDelayHours, IPTWforceDelayMinutes, IPTWdisplayCityName, IPTWdisplayCityIcon, IPTWdisplayObservationTime, IPTWwakeUpOnUpdate, IPTWpreventSleepOnUpdate, IPTWnightIconSuffix, IPTWscheduleNextUpdateOnStart, IPTWdowloadDataAfterStartOnIconTap, IPTWreloadLastDataOnStart
  * Added support for S2U2 as in Moesfeld's weather scripts

### IPTWeather ###

  * first release which should have been named IPTWeather\_20091220