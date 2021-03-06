# Weather Plugin for Elgato StreamDeck

StreamDeck is an awesome productivity tool which allows you almost infinite number of customizations. Therefore, I wanted to develop my own plugin to get updates about the weather.

## What is this plugin about?

Weather Plugin gets and displays weather condition on your StreamDeck hourly from AccuWeather. Its dynamic background changes based on the weather. You can see the full list of backgrounds here https://developer.accuweather.com/weather-icons

This plugin is compatible with both Windows and Mac environments. It is written with the StreamDeck's SDK using JavaScript. 

## Install

Go to https://github.com/tarikguney/weather-plugin-for-elgato-streamdeck/releases and find the latest release. From there, download the `com.tarikguney.weather.streamDeckPlugin` file to your computer. Simply double click on it and it will be automatically installed and be available on StreamDeck application under Custom actions tab.

### Press it for quick updates!

If you press the weather key, you will get the updated weather condition instantly! Otherwise, the weather status will automatically be updated every hour. 

## Settings

You can change the settings using the property inspector pane on StreamDeck application. Let's look at the image below which shows which settings are available and how the plugin looks when working:

![weather-plugin](mainlook.png)

#### `Title`

It does not have any effect. The title is automatically set with the current weather condition including the temperature.

#### `Automatic Refresh`

If you want the weather forecast information to be loaded when the actions are loaded, turn on this setting. However, it comes with some caveats: AccuWeather API, which is used in this plugin to retrieve forecast information, allows only 50 requests per day to be made against their servers. Automatic Refresh may end up hitting this limit faster than the manual retrieval. It is advised to be careful with this option. The times when the automatic refresh will be triggered:

1. StreamDeck is restarting.
2. Switching profiles.

#### `AccuWeather API Key`

Unfortunately, AccuWeather offers only 50 calls per day for each plugin with free AccuWeather accounts. This plugin makes calls to the AccuWeather API to get the hourly weather information to display it on the StreamDeck canvas. Therefore, you need to create your own account and obtain API Key. It is really simple:

1. Create your account here: https://developer.accuweather.com
2. Go to https://developer.accuweather.com/user/me/apps and create an App which will be associated with an API Key that you need to copy and paste here.

Check out the image below:

![api-key-2](key-obtain.png)


#### `Degree Type`

You can set which degree type you'd like to see the temperature in. Currently, the only avaiable options are Celsius and Fahrenheit.

#### `Country Code`

Weather Plugin support international weather forecast report. You can choose whichever country you are in. If you are in the US, the `Zip Code` field will appear. If you are outside of the US, then the `City` field will appear. For instance, type in `London` for the United Kingdom.

#### `Zip Code`

It is pretty clear as to what it is, however, only the USA Zip Codes are supported currently. This field is also known as Postal Code in different parts of the world.

#### `City`

`Zip Code` is not a universal thing so it is replaced with `City` when any country other than the US is selected. City and Zip Code fields show up automatically by which country is chosen. If the location you provided cannot be found, you will be notified.


## Problem?

Please report your issues here https://github.com/tarikguney/weather-plugin-for-elgato-streamdeck/issues. I will be working on this plugin for a while to make it even better. I would appreciate if you let me know the problems you run into during your usage.

## Developed By

@tarikguney with <3

I like my StreamDeck and as a software engineer, it intrigued me to develop something for it. This weather plugin is just a start. I will be adding more plugins, primarily for my own use cases, but I will share them on my Github profile for everyone to use.

## Donation?
If you really like this plugin and buy me a book or something, my PayPal account is atarikguney@gmail.com. 
