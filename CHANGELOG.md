# Changelog M.A.L.P

## 1.2.9 Tag: release-36 (2022-01-09)

* Fix crash on device rotation ([#265](https://gitlab.com/gateship-one/malp/-/issues/265))
* Fix show albums from Files View
* Fix MPD artwork retrieval (bulk download for all music should work now)

## 1.2.8 Tag: release-35 (2021-12-31)

* Migrate to android 12
* Update material components (please raise an issue if themes are broken)
* Hardening of MPD artwork retrieval ([#261](https://gitlab.com/gateship-one/malp/-/issues/261))

## 1.2.7 Tag: release-34 (2020-11-26)

* Add NowPlayingView hint ([#212](https://gitlab.com/gateship-one/malp/-/issues/212))
* Fix duplicated artist name in FanartActivity
* Add support for Seekbar in Notification (starts with Android 10)
* Fix artwork retrieval for HTTP and MPD ([#213](https://gitlab.com/gateship-one/malp/-/issues/213))
* Exclude artworks from backups ([#214](https://gitlab.com/gateship-one/malp/-/issues/214))
* Fix crashes related to MPD artwork retrieval ([#218](https://gitlab.com/gateship-one/malp/-/issues/218), [#134](https://gitlab.com/gateship-one/malp/-/merge_requests/134))

## 1.2.6 Tag: release-33 (2020-09-13)

* Memory usage improvements (mitigates UI freezes due to heavy garbage collection)
* Use a secondary connection to MPD to fetch artwork data (fixes unresponsive MPD connection during fetching)
* Use MPD artwork not only to fetch artwork based on track but also for album overview
* Add support for "readpicture" command of MPD 0.22 (experimental, 0.22 not released yet)
* Fix artist and album grouping on MPD >0.21

## 1.2.5 Tag: release-32 (2020-03-02)

* further improvements for the artwork retrieval
* add prepend to playlist action

## Version 1.2.4 Tag: release-31 (2019-07-14)

* Reenable list grouping for MPD (0.21.11 and above) with new protocol parser (Album artist, MBID, etc support)
* Fix wrong album cover shown if no song is played
* Fix Fanart loading for fullscreen activity when no Musicbrainz IDs are set

## Version 1.2.3 Tag: release-30 (2019-06-18)

* Disable list grouping for all MPD versions >0.21.0 until M.A.L.P. can use list grouping with the changed behavior again

## Version 1.2.2 Tag: release-29 (2019-06-05)

* add hungarian translation (Thanks to Dániel Flórián)
* migrate to AndroidX
* improve artwork retrieval
* remove Last.fm as artist image provider
* fix last updated timestamp in statistics view
* fix several backnavigation issues
* add search view as default view ([#163](https://gitlab.com/gateship-one/malp/issues/163))
* fix aspect ratio of images ([#161](https://gitlab.com/gateship-one/malp/issues/161))

## Version 1.2.1 Tag: release-28 (2018-11-05)

* Hotfix: Workaround for MPD 0.21 (and 0.20.22) protocol breakage. This will reenable MALP with reduced functionality for MPD >=0.21 until a new better solution for album retrieval is found
  * see [MPD bugreport](https://github.com/MusicPlayerDaemon/MPD/issues/408)

## Version 1.2.0 Tag: release-27 (2018-07-12)

* VERY EXPERIMENTAL: MPD inline artwork support. (MPD 0.21 and newer can directly feed MALP album cover artwork over the MPD protocol)
* HTTP-based cover downloading path encoding fixed (#118)

## Version 1.1.17 Tag: release-26 (2018-06-04)

* Migrate to GitLab

## Version 1.1.16 Tag: release-25 (2018-06-02)

* Fix malformed musicbrainz requests
* New settings option to jump directly to playlist view instead of album cover from notification or widget
* Menu entry to manually add a playlist URL to the current playlist. (e.g. use it for soundcloud playlists)

## Version 1.1.15 Tag: release-24 (2018-05-06)

* Add experimental support for ArtistSort & AlbumArtistSort tags
* Updated translations
* Protocol fixes (Escaped strings)

## Version 1.1.14 Tag: release-23 (2018-02-14)

* Stability fixes

## Version: 1.1.13 Tag: release-22 (2018-02-03)

* MPD and connection errors are shown to the user
* Configurable volume button step size
* Default action for library tracks selectable (play song, add song (default), add as next song, details)
* Option to keep the display on when application is active
* Lots of code cleanup and refactoring (especially the MPD connection handling)
* Crash fixes in artist handling
* Updated korean translation
* Hidden feature to open MusicBrainz pages from the song details dialog

## Version: 1.1.12 Tag: release-21 (2017-12-31)

* Experimental feature: local HTTP cover download (see [FAQ](https://github.com/gateship-one/malp/wiki/FAQ))
* Minor bug fixes
* Restructure cover art storage to support larger images (previous downloaded cover art will be lost)
* Improve image processing (scaling and caching)
* Happy new year!

## Version: 1.1.11 Tag: release-20 (2017-11-13)

* Hotfix for: https://issuetracker.google.com/issues/64434571

## Version: 1.1.10 Tag: release-19 (2017-11-10)

* Fix bug: #83
* Follow album sort method in play/add action
* New output selection from NowPlayingView on hold volume button (thanks to sejerpz)
* Statusbar image fix
* Adaptable icon fix
* Widget fix on Android 8

## Version: 1.1.9 Tag: release-18 (2017-10-17)

* Fix bugs: #72, #68
* New sdk version (26)
* Adaptive icon
* Notification channels
* Foreground notification during playback
* Statusbar is currently colored in artist/album view (no fix known at the time)
* Output dialog on longpress on the volume button in NowPlayingView
* Fix for notification image sometimes not showing

## Version: 1.1.8 Tag: release-17 (2017-08-05)

* Stability fixes in UI
* Fix bug #59
* Implement feature request #46
* General stability fixes in current playlist adapter
* Crash fix when entering empty port number in profiles view

## Version: 1.1.7 Tag: release-16 (2017-07-22)

* Stability fixes in UI
* Format MPD dates more nicely
* UI fixes when creating new profiles (new profiles not shown in list)
* Use internal cache instead of external cache for FanartActivity

## Version: 1.1.6 Tag: release-15 (2017-07-10)

* Deidleing with actual timeout to prevent deadlocking/ANR on certain disconnect situations
* UI refinements
* Horizontal resizeable launcher widget

## Version: 1.1.5 Tag: release-14 (2017-06-15)

* Experimental support to play remote streams in M.A.L.P. (http output plugin of MPD for example)
* Small stability fixes

## Version: 1.1.4 Tag: release-13 (2017-03-02)

* French translation (Thanks to Guy de Mölkky)
* UI flickering fixes in ListViews

## Version: 1.1.3 Tag: release-12 (2017-02-05)

* Crash fix on number conversion in MPD connection
* Show artist image in now playing
* Fix multiple profiles created on device rotation
* Reset artwork for one album/artist in their fragment
* Option to reload album / artist image in the corresponing fragments
* Remove visible album sections from current playlist

## Version: 1.1.2 Tag: release-11 (2017-01-15)

* Crash fix in SearchFragment if "Add" button is clicked but no server connection was established
* Crash fix in FanartCache
* Filtering in SavedPlaylists working again
* Workaround for Mopidy's MPD protocol insufficiencies
* Notification enabled by default from now (can be disabled in the settings)
* Artwork is fetched also from the background service
* Small fixes

## Version: 1.1.1 Tag: release-10 (2017-01-10)

* Profile name shown in navigation drawer
* Bugfixes for notification not shown after rotation
* Delayed disconnect on Activity changes
* Save search string on device rotation
* Various crash fixes (reported over play services)
* Single & consume playback option in menu of NowPlayingView
* Japanese translation (thanks to naofum)

## Version: 1.1.0 Tag: release-9 (2016-12-24)

* Launcher widget
* Optional notification if main activity is hidden
* Volume control from outside the application (**only if notification is enabled!**)
* Tablet optimized nowplaying screen
* Album images in playlist view as sections
* Listviews for artists / albums now with images
* Option to change volume slider to volume buttons or disable visible volume controls
* Option to use AlbumArtist tag instead of artist tag for artists list
* Save last used search type in SearchFragment
* Hardware buttons for volume control repeating
* Stabilization of the Artwork downloading
* Fixes for upcoming MPD version 0.20
* Fix of NowPlayingView not shown on Android >=7
