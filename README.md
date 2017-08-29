# Requirements

This skill should work with Mycroft version 0.8.18 +

To use the Pandora ( Pianobar ) skill you'll first need to install Pianobar and configure it to work with your account.  In the future we plan to allow configuration through home.mycroft.ai.

#### First install pianobar package

```
sudo su
apt-get update
apt-get -y install pianobar
exit
```

Now you need to set Pianobar to use the appropriate drivers. Edit the file '/etc/libao.conf' :

```
echo default_driver=pulse > /etc/libao.conf
echo dev=0 >> /etc/libao.conf
```
#### Skill installation
You can install via MSM or git clone this project into the mycroft skills directory usually found in /opt/mycroft/skills

##### MSM
This will install the requirements for you. 

```
msm install pandora
```

##### Manually (git clone)

```
git clone https://github.com/ethanaward/pianobar-skill.git
```
NOTE* If you take this route, you will need to change the permissions on the Mark 1 or Picroft to Mycroft.

```
sudo chown mycroft *
```

```
cd pianobar-skill
```

Install the skill requirements from the requirements.txt

```
pip install -r requirements.txt
```

#### Setting up Pandora Account

create a settings.json file in the root directory of this skill. in file add


```
{
    "email": "YOUR PANDORA EMAIL LOGIN HERE",
    "password": "YOUR PANDORA PASSWORD HERE"
}
```

Once adding settings.json, the skill should reload from the mycroft MSM. If not, restart the skills service.

On Mark 1 and Picroft
```
sudo service mycroft-skills restart
```

On Desktop

```
./mycroft.sh start
```

Now say "Hey Mycroft....play pandora"

## Features

1. Play Pandora 
                
       example "Hey Mycroft... play pandora" or "Hey Mycroft, play Today's Hits Radio"

2. Pause 
    
       example "Hey Mycroft... pause"

3. Resume
    
       example "Hey Mycroft... resume song"

4. Next Song
    
       example "Hey Mycroft... next song"

5. List Stations
    
       example "Hey Mycroft... list stations"

6. Change Stations
    
       example "Hey Mycroft... change station to Today's Top Hits"

7. Next Station
       
       example "Hey Mycroft... next station"


More to come as this project is under active development. 
