# <img src='https://rawgithub.com/FortAwesome/Font-Awesome/master/advanced-options/raw-svg/solid/music.svg ' card_color='#22a7f0' width='50' height='50' style='vertical-align:bottom'/> Pandora
Listen to music from the Pandora music service

## About 
Pandora provides dynamically generated internet radio streams.  Streams are influenced by the the traits of the music played and the songs you like or skip.

Using this Skill does require a [Pandora.com](https://pandora.com) account. Sign-up is free with ad-supported streams.

This Skill should work with Mycroft version 0.9.1 +

### Dependency:  pianobar package

This accesses Pandora via the excellent [pianobar](https://6xq.net/pianobar/) client for Pandora.  The Skill installs the debian package:

```
apt-get update
apt-get -y install pianobar
```

On Picroft and Mark 1, the Skill will automatically set the appropriate drivers. For desktop there is typically no need for driver changes.  If you want to double check, manually do these steps:

```
echo default_driver=pulse > ~/.libao
echo dev=0 >> ~/.libao
```

### Troubleshooting
Debug mode will allow pianobar to write to the mycroft-cli. There you can see a little bit more detail on what pianobar is doing under the hood.  Enable by saying "Pandora debug on"

### FAQ
**Why isn't the song playing?**
* You may be in paused mode.  Try saying 'resume Pandora'
* Sometimes Pandora will deny access to their streaming service. This can be
  resolved by just waiting for some time. I've noticed if i have multiple
  devices playing Pandora at once. To see if this is your issue, turn on debug
  mode, and you should see this message after invoking Pandora 'Error: Access
  denied. Try again later.'
  
**Why does it keep telling me to check my email and password.**
* You should check your email and password.  Really.  Use a browser to log in
  at [Pandora.com](https://pandora.com) to verify you are using the correct
  credentials.

## Examples 
* "Play Pandora"
* "Play Today's Hits Radio on Pandora"
* "Skip this song"
* "Next station"
* "Next song"
* "Pause Pandora"
* "Resume Pandora"
* "Resume Pandora"
* "List my stations"
* "Next station"
* "Change station to Today's Top Hits on Pandora"

## Credits 
Mycroft AI (@MycroftAI)

## Category
**music**

## Tags
#pandora
#music
#streaming-music
#pianobar
