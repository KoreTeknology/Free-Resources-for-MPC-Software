[<< Back to main page](/../..)

---

# Drumsynth Models API (2.11x)

## Basic structure of the XPL Presets, ADSM & ADSS Files Contents

Each preset is composed from several parameters and values. We must note that basicaly each type of instruments has differents parameters! Let´s look first at the basic principle of models per type. Each model contains a structured content, including parameters and data.<br>
**.adsm** = Air Drum Synth Model<br>
**.adss** = Air Drum Synth Structure

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

 <b>* is that binary data ? 0/1, for what ? most models contain this <i>null</i> data</b>
 
 
## File structure (.adsm file type)
  
```diff 
ParamOffest 1 (optional)
Macro  0  Param  257  0.01736  0.9556  0  Def  0.0805  Tune
Macro  1  Param  255  0.00     0.50    0  Def  0.50    Hold
...
Pitch  257 (optional)
```

 ---

### Available Parameters Table

<table>
<tr>
<th align="center", width="20">Num.</th>
<th align="left", width="180">Parameters</th>
<th align="left", width="600">Description</th>
<th align="center", width="180">Value Range</th>
<th align="center", width="90">ID</th>
</tr>
<tr>
 <td  align="center", valign="top"><b>1</b></td><td  valign="top"><b>Tune</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>2</b></td><td  valign="top"><b>Hold</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>3</b></td><td  valign="top"><b>Decay</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>4</b></td><td  valign="top"><b>Sweep</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>5</b></td><td  valign="top"><b>Sweep-Decay</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>6</b></td><td  valign="top"><b>Sweep-Depth</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>7</b></td><td  valign="top"><b>Harm</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>8</b></td><td  valign="top"><b>Punch</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>9</b></td><td  valign="top"><b>Drive</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>10</b></td><td  valign="top"><b>Attack</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>11</b></td><td  valign="top"><b>Body</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>12</b></td><td  valign="top"><b>Beat</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>13</b></td><td  valign="top"><b>Beat-Color</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>14</b></td><td  valign="top"><b>Beat-Mid</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>15</b></td><td  valign="top"><b>Hit</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>16</b></td><td  valign="top"><b>Noise</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>17</b></td><td  valign="top"><b>Noise-Color</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>18</b></td><td  valign="top"><b>Noise-Resonance</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>19</b></td><td  valign="top"><b>Noise-Dec</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>20</b></td><td  valign="top"><b>Click</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>21</b></td><td  valign="top"><b>Clip</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>22</b></td><td  valign="top"><b>Character</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>23</b></td><td  valign="top"><b>Soft</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>24</b></td><td  valign="top"><b>Hi-Hat</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>25</b></td><td  valign="top"><b>HH-Dec</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>26</b></td><td  valign="top"><b>HH-Tune</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>27</b></td><td  valign="top"><b>Att-Noise</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>28</b></td><td  valign="top"><b>Att-Time</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>29</b></td><td  valign="top"><b>Att-Dirt</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>30</b></td><td  valign="top"><b>Spike</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>31</b></td><td  valign="top"><b>Complex</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>32</b></td><td  valign="top"><b>Balance</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>33</b></td><td  valign="top"><b>FM-Tune</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>34</b></td><td  valign="top"><b>FM-Depth</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>35</b></td><td  valign="top"><b>Tone</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>36</b></td><td  valign="top"><b>Flam</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>37</b></td><td  valign="top"><b>Mix</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>38</b></td><td  valign="top"><b>Stereo</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>39</b></td><td  valign="top"><b>Harmonize</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>40</b></td><td  valign="top"><b>Complx-Dec</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>41</b></td><td  valign="top"><b>Stick</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>42</b></td><td  valign="top"><b>Dens</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>43</b></td><td  valign="top"><b>Pitch</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>44</b></td><td  valign="top"><b>Pitch-Dec</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>45</b></td><td  valign="top"><b>Spike-Len</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>46</b></td><td  valign="top"><b>Bandpass</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>47</b></td><td  valign="top"><b>Reso</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>48</b></td><td  valign="top"><b>HiPass</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  align="center", valign="top"><b>49</b></td><td  valign="top"><b>Metal</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.999 to 0.999</td><td align="center"  valign="top">000</td>
</tr>
<table>

