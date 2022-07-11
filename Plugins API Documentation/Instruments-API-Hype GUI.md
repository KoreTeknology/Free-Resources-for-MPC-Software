# API Hype Plugin

![akai link](https://d1jtxvnvoxswj8.cloudfront.net/wysiwyg/akai-pro/pdp/mpc-air-hype-synth/mpc-air-hype-synth-collage-a.png)

The **"HYPE PLUGIN SKINS"** folder includes:

## The background:

| BACKGROUNDS | Page 1  | Page 2  | Page 3  | Page 4  | Page 5  | Dimensions (px) |
| --- | --- | --- | --- | --- | --- | :---: |
| BG Pages: | fbank_01.png | fbank_02.png | fbank_03.png | fbank_04.png | fbank_05.png | **1280x629** |

## The Switch buttons:

| GUI Elements: Switches (Buttons with 2 states) | Images OFF  | Images ON  | Dimensions (px) |
| --- | --- | --- | :---: |
| Compressor Switch: | comp_off.png  |  comp_on.png | **213x70** |
| Delay Switch: | delay_off.png  |  delay_on.png | **213x70** |
| Distortion Switch: | dist_off.png  |  dist_on.png | **213x70** |
| Fx Switch: | fx_off.png  |  fx_on.png | **10x10** |
| Hype Switch: | hype_off.png  |  hype_on.png | **213x70** |
| Lfo Switch: | lfo_off.png  |  lfo_on.png | **68x58** |
| Limiter Switch: | limit_off.png  |  limit_on.png | **213x70** |
| Modulation Switch: | mod_off.png  |  mod_on.png | **213x70** |
| Pump Switch: | pump_off.png  |  pump_on.png | **213x70** |
| Reverb Switch: | reverb_off.png  |  reverb_on.png | **213x70** |

## The Sliders and Knobs:

| GUI Elements: Sliders & Knobs (Vertical steps) | Images  | Dimensions (px) |
| --- | --- | :---: |
| Cylinder Slider: | cylinder.png  | **180x15240** |
| Diamond Slider: | diamond.png  | **180x15240** |
| Hexagon Slider: | hexagon.png  | **180x15240** |
| Mix Slider: | mix.png  | **180x15240** |
| Pyramid Slider: | pyramid.png  | **180x15240** |
| Square Slider: | square.png  | **180x15240** |
| Hype Hi Slider: | hype_hi.png  | **98x61722** |
| Hype Low Slider: | hype_low.png  | **98x61722** |
| Hype X-hi Slider: | hype_xhi.png  | **98x61722** |
| Hype X-low Slider: | hype_xlow.png  | **98x61722** |
| Slider: | slider.png  | **40x24638** |
| Knob: | knob.png  | **70x8890** |
| Large knob: | knob_lg.png  | **87x11136** |
| Setup knob: | softknob_setup.png  | **26x3302** |
| Blue knob: | softknob_blue.png  | **41x5207** |
| Green knob: | softknob_green.png  | **26x3302** |

## The structured data/setup files:

| GUI structure: JSON files |  Data | Weight (Kb) |
| --- | --- | :---: |
| Main: | TUI.json  | **326** |
| Qlinks: | Q-Links.json | **4.27** |
| Extra: | Q-Links - 8by1.json | **4.27** |

---

# Customizations and Compositions

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

Now, we understand how to modify our plugin GUI, to accomodate the design to our preferences. The next step is start applying changes, but before that, dont forget to make a copy of the original folder !!! Let´s go for the plugin **"HYPE"** :) I personaly dont like the original design of this nice little synth, the poor and non-logical graphic design and the complete chaos in the page contents organisation... but this is how i feel, doesn t mean we are equal on those feelings.

It has 5 pages in a row, from left to right **(6400x629px)**, this is a huge surface!
Let´s look at the first page, **6 main controls** with strange shapes with basic synthesis params, **8 controls** for filter, distortions, Fx and Master Volume, and a **set of switches** for each section of the synth. Well, let´s try something simple, edit the first param-control: **"layer {oscillators} mix"**!

---

Open the **TUI.json** file included into the theme folder.
Where are located the content for this control in this file? search for:

### from Page 1 "MACRO" (componentDefinitions), Line 1047:
```yaml
{
                    "key": "mix",
                    "value": {
                        "version": 1,
                        "actions": [
                            {
                                "version": 1,
                                "onAction": "Mouse Down",
                                "handler": "Q-Link",
                                "handleName": "Data",
                                "additionalData": ""
                            },
                            {
                                "version": 1,
                                "onAction": "Double Click",
                                "handler": "Show Overlay",
                                "handleName": "",
                                "additionalData": "knob overlay"
                            },
                            {
                                "version": 1,
                                "onAction": "Enter Pressed",
                                "handler": "Show Overlay",
                                "handleName": "",
                                "additionalData": "knob overlay"
                            }
                        ],
                        "backgroundData": {
                            "version": 1,
                            "focussed": {
                                "version": 1,
                                "colour": "0",
                                "image": ""
                            },
                            "unfocussed": {
                                "version": 1,
                                "colour": "0",
                                "image": ""
                            }
                        },
                        "ignoreMousePresses": false,
                        "componentsData": [
                            {
                                "version": 1,
                                "componentData": {
                                    "version": 1,
                                    "name": "Focus",
                                    "type": "Focus",
                                    "data": {
                                        "version": 1,
                                        "backgroundColour": "08ffffff",
                                        "outlineColour": "ffe81f40",
                                        "backgroundInset": 4.0,
                                        "outlineThickness": 1.0
                                    }
                                },
                                "version": 1,
                                "map": [],
                                "bounds": {
                                    "version": 1,
                                    "acceptsHWFocus": "No",
                                    "showWhenDataModelInvalid": "Show",
                                    "whenVisible": "WhenFocussed",
                                    "boundsType": "Absolute",
                                    "bounds": "0 0 190 165"
                                }
                            },
                            {
                                "version": 1,
                                "componentData": {
                                    "version": 1,
                                    "name": "Knob",
                                    "type": "Knob",
                                    "data": {
                                        "version": 1,
                                        "knobType": "FilmStrip",
                                        "filmStrip": "mix.png",
                                        "numFrames": 127,
                                        "handleName": "Data"
                                    }
                                },
                                "version": 1,
                                "map": [],
                                "bounds": {
                                    "version": 1,
                                    "acceptsHWFocus": "No",
                                    "showWhenDataModelInvalid": "Show",
                                    "whenVisible": "Always",
                                    "boundsType": "Absolute",
                                    "bounds": "5 5 180 120"
                                }
                            },
                            {
                                "version": 1,
                                "componentData": {
                                    "version": 1,
                                    "name": "Label",
                                    "type": "Label",
                                    "data": {
                                        "version": 1,
                                        "textStyle": {
                                            "version": 1,
                                            "font": {
                                                "version": 1,
                                                "name": "Titillium Web",
                                                "style": "SemiBold",
                                                "height": 30
                                            },
                                            "colour": "fffffffff",
                                            "justification": "horizontallyCentred verticallyCentred",
                                            "case": "Original"
                                        },
                                        "type": "Value",
                                        "handleName": "Data"
                                    }
                                },
                                "version": 1,
                                "map": [],
                                "bounds": {
                                    "version": 1,
                                    "acceptsHWFocus": "No",
                                    "showWhenDataModelInvalid": "Show",
                                    "whenVisible": "Always",
                                    "boundsType": "Absolute",
                                    "bounds": "0 130 190 30"
                                }
                            }
                        ]
                    }
},
```

---

### from Page 1 "MACRO" (tabs), Line 3534:
```yaml
{
                            "version": 1,
                            "componentData": {
                                "version": 1,
                                "name": "Layer Mix",
                                "type": "mix",
                                "data": {
                                    "version": 1,
                                    "handleName": "Data"
                                }
                            },
                            "version": 1,
                            "map": [
                                {
                                    "key": "Data",
                                    "value": "Parameter 0"
                                }
                            ],
                            "bounds": {
                                "version": 1,
                                "acceptsHWFocus": "Yes",
                                "showWhenDataModelInvalid": "Hide",
                                "whenVisible": "Always",
                                "boundsType": "Absolute",
                                "bounds": "121 57 190 165"
                            }
},
```
---

First of all, we have here a **component (layer mix)** that includes several caracteristics:
- **"actions"**: Mouse Down, Double Click, Enter Pressed
- **"backgroundData"**: focused, unfocused
- **"componentsData"**: Focus, Knob, Label

What are we interested for? we will look at the **boudary location** of the control´s bloc in the tabs section:
```yaml
"boundsType": "Absolute",
"bounds": "121 57 190 165"
```
and then we enter the **graphical space** of the control elements:
```yaml
Focus: "bounds": "0 0 190 165"
Knob: "bounds": "5 5 180 120"
Label: "bounds": "0 130 190 30"
```
We also know the **size of the image file** we are up to load for the **knob** element:
```yaml
"knobType": "FilmStrip",
"filmStrip": "mix.png",
"numFrames": 127,
```

---

This image "mix.png" is **180x15240px**, **127 vertical steps**, so one step image is **180x120px (WxH)**.
Each boudary statement is base on the top-left corner, that means the first pixel on the top left corner of the GUI is located at **0,0**; and the last bottom-right corner is located at **1278,628**.

We may look now at how to replace this image by creating a new file (*using [Photoshop](https://www.adobe.com/products/photoshop.html) or [Gimp](https://www.gimp.org/)*).
I am creating a template for my **knob**, adding markers between each steps to delimitate the area available for each sequenced images. The final image file contains **127 variations steps** of the knob´s rotation.

Ok, it works, it is fine but let´s go futher. i want to move this knob and its component´s elements to be aligned on the left side of the page. I will place it at **10,10**. I also want to change the aspect of the image to be **150x150px**, change the color of the bottom data.

