@codeeshop/cordova-plugin-google-play-games [![Latest Stable Version](https://img.shields.io/npm/v/@codeeshop/cordova-plugin-google-play-games.svg)](https://www.npmjs.com/package/@codeeshop/cordova-plugin-google-play-games) [![Total Downloads](https://img.shields.io/npm/dt/@codeeshop/cordova-plugin-google-play-games.svg)](https://npm-stat.com/charts.html?package=@codeeshop/cordova-plugin-google-play-games)
========================

## Table of Contents

- [Install](#install)
- [Common Issues](#common-issues)
- [Reference](#reference)

-------- 

## Install

Step 1. Find games-ids.xml File Content from Google Play Developer Page (Link will be like below)
https://play.google.com/console/u/0/developers/...................../games/configuration-summary

Step 2. Add File Under Path

```bash
res/android/values/games-ids.xml
```

#### Example Content File

```bash
<?xml version="1.0" encoding="utf-8"?>
<!--Google Play game services IDs. Save this file as res/values/games-ids.xml in your project.-->
<resources>
  <!--app_id-->
  <string name="app_id" translatable="false">XXXXXXXXXXXX</string>
  <!--package_name-->
  <string name="package_name" translatable="false">com.xxxxxxxxxx.app</string>
  <!--achievement Started-->
  <string name="achievement_started" translatable="false">CgkXXXXXXXXXX</string>
  <!--event 1 Word Solved-->
  <string name="event_1_word_solved" translatable="false">CgkXXXXXXXXXX</string>
  <!--leaderboard Highest World Solved-->
  <string name="leaderboard_highest_world_solved" translatable="false">CgkXXXXXXXXXX</string>
</resources>
```
Step 3. Update config.xml 

```bash
<resource-file src="res/android/values/games-ids.xml" target="/app/src/main/res/values/games-ids.xml" />
```
Step 4. Add Plugin

```bash
cordova plugin add @codeeshop/cordova-plugin-google-play-games
```

## Common Issues

Login Failed Issues

#### Resolutions
Make sure your sha1 key is valid
Setup > App signing ( Check for App signing key certificate > SHA-1 certificate fingerprint )
![Screenshot from 2023-10-23 14-57-43](https://github.com/codeeshop-oc/cordova-plugin-google-play-games/assets/54684361/e7bf9c66-74de-4cec-942d-66fa514981bd)

## Reference

[maximnara/cordova-plugin-google-play-games](https://github.com/maximnara/cordova-plugin-google-play-games)
