# PlexMusic-Skill
FORKED FROM COLLA69
<img src="https://assets.pcmag.com/media/images/517012-plex-logo.png?width=333&height=245" align="right">

### Description

This Mycroft skill can play music from your plex media server with speech commands.

### Requirements
  you will need access to a plex media server and a working version of the vlc player.
  
  ##### how to get vlc:
  Debian/Ubuntu `sudo apt install vlc-bin`  
  CentOs        `sudo yum install vlc-bin`  
  Arch/Manjaro  `sudo pacman -S vlc-bin`   
    
### Install
  `msm install https://github.com/rbcolom/plexmusic-skill.git`
  
### Examples
 - "Hey mycroft, play mockingbird!"
 - "Hey mycroft, play eminem!"
 - "Hey mycroft, play album meteora"
 
### Functions
  - Play *song|artist|album name*
  - Play *artist name*    
  - Play *album name*    
  - Play *playlist name*    
  - Pause music
  - Resume music
  - Next|Skip
  - Reload|Refresh library 

### Usage
  Once you have installed the skill, go to https://account.mycroft.ai/skills and find the Plex Music Skill.<br>
  Please fill in the 3 fields:
   - plex uri (address of your PlexMediaServer, it has to be reachable on port 32400)
    <br>e.G. http://my.plex.address 
   - plex token (for info visit https://support.plex.tv/articles/204059436-finding-an-authentication-token-x-plex-token/)
   <br>e.G. ys738s6uPWXpwabc4sRYe
   - Library name in plex  (the name of the library to play the music from)
   <br>e.G. Music
  
  Alternative config (mycroft.conf):<br>
  ```json
  "plexmusic-skill": {
    "musicsource": "http://my.plex.address",
    "plextoken": "ys738s6uPWXpwabc4sRYe", 
    "plexlib": "music", 
    "ducking": true
  }
  ```
  
  
  The first intallation will need to download all your library metadata and will save it in a JSON file. 
  (~/.config/plexSkill/data.json) <br> 
  The process will take a long time, don't panic, you can watch it load if you have debug=True in your config. 

### Credits
colla69


