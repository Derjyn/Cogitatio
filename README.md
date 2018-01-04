# Cogitatio

Cogitatio is a suite of plugins for Unreal Engine that operate independently of each other, but are capable of empowering one another, exposing new features when present. Rector is an optional plugin that will detect any other Cogitatio plugins and expose settings or functionality in a categorical manner for ease-of-use, as well as optionally handle the initialization, update, shutdown, etc of the plugins. The goal here is a more streamlined workflow, with a "finger on the pulse" of the plugin life cycle.

Below is a list of the plugins currently in the development, followed by a short description of each. You may have noticed that a latin naming scheme was chosen. The rough translation is available in the descriptions for each plugin. Cogitatio itself roughly translates as "_thought, plan, design_".

* Aer (alpha)
* Auxilium (concept)
* Capsa (concept)
* Fera (concept)
* Hora (beta)
* Medela (concept)
* Rector (alpha)
* Sensus (concept)

-----

### Aer
_air, climate, atmosphere_

Aer is a weather and atmospherics plugin. Originally, night and day cycle functionality was going to be handled in Hora, but weather and atmospherics have such a close relationship with the sun and moon, that it made more sense to move that functionality into Aer. On top of weather, atmospherics, and night/day cycles, other visual (and not-so-visual) elements such as shooting stars are in the works.

### Auxilium
_aid, support, resource_

Auxilium is an infrastructure plugin. Types of resources can be defined, which are utilized by other actors (referred to as an **appliance**) to modify functionality. A simple example would be a **generator appliance** requiring the presence of a **fuel resource**. A third type in the mix is an **alterant**, which can modify the traits of resources and appliances. Appliances can require more than one resource, and can even generate a new resource, based on the input resources and alterants.

### Capsa
_locker, chest, holder_

Capsa is an inventory plugin. While at a basic level, your run-of-the-mill inventory system can be created using Capsa, the higher-level goal of physical inventory items was conceptualized. Inventory objects (such as weapons, ammo, food, etc) have weight, take up volume, and can effect the world around them more than a simple icon on a bar or in a menu. A lot of thought is going into Capsa, with the vision to give more tangible value to items a player might acquire.

### Fera
_wild beast, animal_

Fera is an ambient and active wildlife simulation plugin. Inspired heavily by the ALife system in the classic S.T.A.L.K.E.R. games, the vision for Fera is to have wildlife that interacts with the environment and other parts of nature, as well as the player. Animals that hunt or flee from danger are nothing new, but those interactions have also been binary for the most part. A wolf in an MMORPG is generally idling, until the player comes near, at which point it attacks, until the player hurts it enough, in which case it flees. Idle, hunt/attack, flee... Fera means to enable more complex wildlife, offering more levels of interesting behaviors that feel more alive.

### Hora
_hour, time, season_

Hora is a performant date and time plugin. Dozens of helpful Blueprint nodes are made available for getting the time, date, season, etc. Events for the passage of seconds, minutes, hours, and so on are also available, as well as time-of-day changes (morning, afternoon, etc). Annual (once yearly) and custom (once on a specific day/month/year) date events can be added easily as well. Julian date is calculate, Julian days since epoch dates (currently J2000), and season days (days into the current season) as well as season value (normalized value from 0-1 of current season passage) are also available.

### Medela
_remedy, health_

Medela is a health plugin, with injury and diseases. Injuries, diseases, and mental health can have effects on a character's traits, which are also a part of Medela. Medela is in the concept stages currently.

### Rector
_ruler, guide, controller_

Rector is a utility plugin, that detects any other active Cogitatio plugins and organizes their settings and functionality in the Unreal Engine editor for easier access. It is also capable of handling the life of a plugin: the startup, update, and shutdown, if desired. A high-level goal with each Cogitatio plugin is to make them self-managing by default, but allow you to manually handle their lifetime if desired. If enabled in Rector's settings, any plugins set to be self-managed will be watched by Rector and optimally started, updated and stopped.

### Sensus
_feeling, thought, disposition_

With Fera handling "wildlife" simulation, we have Sensus handling the more human side of artificial life. The goal with Sensus is to give NPCs memory, unique attitudes, likes/dislikes, and so on. By developing a few basic needs, desires and fears for an NPC, the level of interaction with an otherwise cookie-cutter armor vendor can suddenly become quite interesting. The effects of player choices and world events can give rise to more emergent gameplay. Very much in the concept stages.
