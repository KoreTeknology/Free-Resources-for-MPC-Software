# API - Air Instruments Plugins

*(Last updated: 08/07/2022)*

This document presents the keys and values associated with the interactive components of the user interfaces of AIR plugins, present in the latest versions of Akai MPC software. You will find here all the reference information to develop your own graphic themes.

---

## General structure

All plugin´s themes are constructed in the same way, thanks to a list of references (parameters) and a list of components (controls). Each plugin then has a JSON file which links these elements.


- **[Drumsynth Plugins Models References]()**
    - **[Drumsynth Kick Plugin References]()**
    - **[Drumsynth Snare Plugin References]()**
    - **[Drumsynth Hihat Plugin References]()**
    - **[Drumsynth Clap Plugin References]()**
    - **[Drumsynth Percussion Plugin References]()**
    - **[Drumsynth Tom Plugin References]()**
    - **[Drumsynth Crash Plugin References]()**
    - **[Drumsynth Ride Plugin References]()**
    - **[Drumsynth Multi Plugin References]() - [Presets](Instruments-API-Drumsynth%20Multi%20Presets.md) - [Gui](Instruments-API-Drumsynth%20Multi%20GUI.md)**
- **[Solina Plugin References]() - Presets - [Gui](Instruments-API-Solina%20GUI.md)**
- **[Hype Plugin References]() - Presets - [Gui](Instruments-API-Hype%20GUI.md)**
- **[Mellotron Plugin References]()**
- **[Odyssey Plugin References]()**
- **[Electric Plugin References]()**
- **[Tubesynth Plugin References]()**
- **[Bassline Plugin References]()**

---

## Customizations and Compositions

Before we do any modification to the plugin, let s have a look at the **design file** structure. We will use this JSON programming language all over this tutorial, if you are not familiar with it, i suggest you to visit the [Introducing JSON Website](https://www.json.org/json-en.html) and learn from the ground how it is made and what are the benefit of using this data file format.

The main Object is a **"PageData" container**, it has 4 sections:
- version
- componentDefinitions
- info
- tabs

Each one contains some sort of data to publish a user interface for the plugin.
```diff 
! from there, you must understand that we cannot add more features than it has before
! you can only change the visual aspect of the GUI elements !!!
```

---

**Let´s see in detail, what is there and what we can do or modify to get the desired effect or interface composition.**

- [x] The "version" section only contains a single number as "data object referencing tag".

- [x] The "componentDefinitions" first load some external files as libraries, then describe all the components or graphical elements on the plugin that do an action or interaction with the user. It is based on key-value relationship by design.

- [x] The "info" section presents the type of content, it can be a main file or a secondary file.

- [x] The "tabs" section presents the general images structure, by placing accuratly the graphics at the good place and at the good size. This section is especialy interesting because of the potential of moving controls and re-structure the whole plugin*

*by this technique, you can make a single page plugin and place all the controls over it ;)
```diff 
- Dont create a plugin that will not fit the Akai MPC Software maximum dimensions in pixels > 1280x629px
```
---
