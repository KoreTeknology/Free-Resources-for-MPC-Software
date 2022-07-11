[<< Back to main page](/../..)

---

# Kick Models API (2.11x)

## Available Synthesis Models

Model Name | Parameters | .adsm file | .adss file | Default |
:--------------------------------------- | :--- | :---: | :---: |:---: |
Eighty | *Tune, Hold, Decay, Sweep, Harm, Click, Noise, Noise-color* | Eighty.adsm | Eighty.adss |:heavy_check_mark: |
Ninety | *Tune, Hold, Decay, Sweep, Punch, Harm, Click, Noise* | Ninety.adsm | Ninety.adss |:heavy_check_mark: |
Driven 8 | *Tune, Hold, Decay, Sweep-Decay, Sweep-Depth, Punch, Harm, Drive* | Driven8.adsm | Driven8.adss |:heavy_check_mark: |
Hybrid | *Tune, Hold, Decay, Sweep, Punch, Att-Noise, Att-Time, Att-Dirt* | Hybrid.adsm | Hybrid.adss |:heavy_check_mark: |
Transe | *Tune, Hold, Decay, Hit, Sweep, Sweep-Dec, Noise, Noise-Col* | Transe.adsm | Transe.adss |:heavy_check_mark: |
Natural A | *Tune, Decay, Attack, Body, Beat, Beat-Color, Noise, Noise-Reso* | NaturalA.adsm | NaturalA.adss |:heavy_check_mark: |
Natural B | *Tune, Decay, Body, Beat, Beat-Mid, Noise, Noise-Dec, Noise-Col* | NaturalB.adsm | NaturalB.adss |:heavy_check_mark: |
Hard 1 | *Tune, Hold, Decay, Harm, Dist, Beat, High, Noise* | Hard1.adsm | Hard1.adss |:heavy_check_mark: |
Hard 2 | *Tune, Hold, Decay, Sweep, Click, Hi-Hat, HH-Dec, HH-Tune* | Hard2.adsm | Hard2.adss |:heavy_check_mark: |
Clipped | *Tune, Hold, Decay, Sweep, Clip, Character, Soft, Click* | Clipped.adsm | Clipped.adss |:heavy_check_mark: |
Custom 1 | *Tune, Hold, Decay, Sweep, Clip, Character, Soft, Noise* | Custom1.adsm | Custom1.adss |:x: |

## Kick Models Instrument Definition

<table>
 <tr><H3>EIGHTY / Param. Offset Data Table (.adsm file type)</h3></tr>
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
 <td align="center">Data Level</td>
 <td align="center">Param. Order</td>
 <td align="center">Separator /</td>
 <td align="center">Parameter ID</td>
 <td align="center">Minimum Value</td>
 <td align="center">Maximum Value</td>
 <td align="center">Null</td>
 <td align="center">Separator /</td>
 <td align="center">Default Value</td>
 <td align="center">Param. Name</td>
</tr>
<tr>
 <td><b>Type:</b></td>
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

```diff 
ParamOffest 1
Macro  0  Param  257  0.01736  0.9556  0  Def  0.0805  Tune
Macro  1  Param  255  0.00     0.50    0  Def  0.50    Hold
```


