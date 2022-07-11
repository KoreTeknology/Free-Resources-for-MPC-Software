[<< Back to main page](/../..)

---

# Drumsynth Models API (2.11x)

## Basic structure of the XPL Presets, ADSM & ADSS Files Contents

Each preset is composed from several parameters and values. We must note that basicaly each type of instruments has differents parameters! Let´s look first at the basic principle of models per type. Each model contains a structured content, including parameters and data.<br>
**.adsm** = Air Drum Synth Model<br>
**.adss** = Air Drum Synth Structure

### Parameters Table

<table>
<tr>
<th align="left", width="130">Parameters</th>
<th align="left", width="650">Description</th>
<th align="center", width="180">Range</th>
<th align="center", width="90">ID</th>
</tr>
<tr>
 <td  valign="top"><b>Tune</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Hold</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Decay</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Sweep</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Sweep-Decay</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Sweep-Depth</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Harm</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Punch</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Drive</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Attack</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Body</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Beat</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Beat-Color</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Hit</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Noise</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Noise-Color</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Noise-Resonance</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Noise-Dec</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Click</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Clip</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Character</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Soft</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Hi-Hat</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>HH-Dec</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>HH-Tune</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<table>

<table>
 <tr><H3>Param. Offset Data / Models Content Table</h3></tr>
<tr>
<th align="left", width="120">Column:</th>
<th align="center", width="60">1</th>
<th align="center", width="60">2</th>
<th align="center", width="60">3</th>
<th align="center", width="60">4</th>
<th align="center", width="120">5</th>
<th align="center", width="120">6</th>
<th align="center", width="60">7</th>
<th align="center", width="60">8</th>
<th align="center", width="120">9</th>
<th align="center", width="60">10</th>
</tr>
<tr>
 <td><b>Content:</b></td>
 <td align="center">Level</td>
 <td align="center">Order</td>
 <td align="center">Type</td>
 <td align="center">Type Value</td>
 <td align="center">Minimum Value</td>
 <td align="center">Maximum Value</td>
 <td align="center">?*</td>
 <td align="center">Def</td>
 <td align="center">Default Value</td>
 <td align="center">Name</td>
</tr>
<tr>
 <td><b>Data type:</b></td>
 <td align="center">STRING</td>
 <td align="center">INTEGER</td>
 <td align="center">STRING</td>
 <td align="center">INTEGER</td>
 <td align="center">FLOAT</td>
 <td align="center">FLOAT</td>
 <td align="center">INTEGER</td>
 <td align="center">STRING</td>
 <td align="center">FLOAT</td>
 <td align="center">STRING</td>
</tr>
 <tr>
 <td><b>Exemple:</b></td>
 <td align="center">Macro</td>
 <td align="center">2</td>
 <td align="center">Param</td>
 <td align="center">255</td>
 <td align="center">0.01736</td>
 <td align="center">0.9556</td>
 <td align="center">0</td>
 <td align="center">Def</td>
 <td align="center">0.50</td>
 <td align="center">Hold</td>
</tr>
<table>

 <b>* is that binary data ? 0/1, for what ? most models contain this <i>null</i> data</b>
 
 
## File structure (.adsm file type)
  
```diff 
ParamOffest 1 (optional)
Macro  0  Param  257  0.01736  0.9556  0  Def  0.0805  Tune
Macro  1  Param  255  0.00     0.50    0  Def  0.50    Hold
...
Pitch  257 (optional)
```
