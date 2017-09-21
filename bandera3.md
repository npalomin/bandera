

```python
import pandas as pd
import numpy as np
```


```python
width = pd.read_csv('N:\\bandera\GIS\Intersect_MAN.csv')
```


```python
width.head(5)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>keyman</th>
      <th>heading</th>
      <th>length</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>432.257263</td>
      <td>49.999986</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>355.762207</td>
      <td>15.970360</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>289.011902</td>
      <td>18.414908</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>273.227387</td>
      <td>17.759665</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>273.227387</td>
      <td>12.740908</td>
    </tr>
  </tbody>
</table>
</div>




```python
width.groupby('keyman').sum()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>heading</th>
      <th>length</th>
    </tr>
    <tr>
      <th>keyman</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>432.257263</td>
      <td>49.999986</td>
    </tr>
    <tr>
      <th>2</th>
      <td>355.762207</td>
      <td>15.970360</td>
    </tr>
    <tr>
      <th>3</th>
      <td>289.011902</td>
      <td>18.414908</td>
    </tr>
    <tr>
      <th>4</th>
      <td>546.454773</td>
      <td>30.500572</td>
    </tr>
    <tr>
      <th>5</th>
      <td>705.372375</td>
      <td>30.922796</td>
    </tr>
    <tr>
      <th>6</th>
      <td>543.621704</td>
      <td>30.119842</td>
    </tr>
    <tr>
      <th>7</th>
      <td>709.983154</td>
      <td>29.987797</td>
    </tr>
    <tr>
      <th>8</th>
      <td>543.704651</td>
      <td>29.970359</td>
    </tr>
    <tr>
      <th>9</th>
      <td>707.604797</td>
      <td>30.524197</td>
    </tr>
    <tr>
      <th>10</th>
      <td>545.307007</td>
      <td>30.205787</td>
    </tr>
    <tr>
      <th>11</th>
      <td>290.861359</td>
      <td>18.618315</td>
    </tr>
    <tr>
      <th>12</th>
      <td>639.830261</td>
      <td>11.671712</td>
    </tr>
    <tr>
      <th>13</th>
      <td>290.987732</td>
      <td>19.908398</td>
    </tr>
    <tr>
      <th>14</th>
      <td>447.766144</td>
      <td>42.421337</td>
    </tr>
    <tr>
      <th>15</th>
      <td>707.970093</td>
      <td>35.095815</td>
    </tr>
    <tr>
      <th>16</th>
      <td>758.283997</td>
      <td>43.471505</td>
    </tr>
    <tr>
      <th>17</th>
      <td>579.004700</td>
      <td>40.909929</td>
    </tr>
    <tr>
      <th>18</th>
      <td>708.568848</td>
      <td>31.654263</td>
    </tr>
    <tr>
      <th>19</th>
      <td>709.503418</td>
      <td>29.725316</td>
    </tr>
    <tr>
      <th>20</th>
      <td>376.520966</td>
      <td>21.417722</td>
    </tr>
    <tr>
      <th>21</th>
      <td>715.051758</td>
      <td>31.271249</td>
    </tr>
    <tr>
      <th>22</th>
      <td>894.614258</td>
      <td>43.705464</td>
    </tr>
    <tr>
      <th>23</th>
      <td>290.181641</td>
      <td>19.762129</td>
    </tr>
    <tr>
      <th>24</th>
      <td>890.455872</td>
      <td>29.978223</td>
    </tr>
    <tr>
      <th>25</th>
      <td>887.825195</td>
      <td>40.852763</td>
    </tr>
    <tr>
      <th>26</th>
      <td>708.030457</td>
      <td>41.075675</td>
    </tr>
    <tr>
      <th>27</th>
      <td>888.421509</td>
      <td>25.002015</td>
    </tr>
    <tr>
      <th>28</th>
      <td>887.684814</td>
      <td>41.604935</td>
    </tr>
    <tr>
      <th>29</th>
      <td>706.930481</td>
      <td>28.006966</td>
    </tr>
    <tr>
      <th>30</th>
      <td>889.027344</td>
      <td>29.837683</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>4292</th>
      <td>367.207886</td>
      <td>14.010817</td>
    </tr>
    <tr>
      <th>4295</th>
      <td>705.553955</td>
      <td>35.181797</td>
    </tr>
    <tr>
      <th>4296</th>
      <td>717.036804</td>
      <td>26.739740</td>
    </tr>
    <tr>
      <th>4297</th>
      <td>288.711792</td>
      <td>0.262377</td>
    </tr>
    <tr>
      <th>4298</th>
      <td>356.460205</td>
      <td>19.883937</td>
    </tr>
    <tr>
      <th>4299</th>
      <td>289.867371</td>
      <td>1.613107</td>
    </tr>
    <tr>
      <th>4304</th>
      <td>710.465515</td>
      <td>18.823122</td>
    </tr>
    <tr>
      <th>4312</th>
      <td>276.834259</td>
      <td>14.714256</td>
    </tr>
    <tr>
      <th>4314</th>
      <td>430.449219</td>
      <td>10.273627</td>
    </tr>
    <tr>
      <th>4315</th>
      <td>428.451172</td>
      <td>13.969402</td>
    </tr>
    <tr>
      <th>4316</th>
      <td>431.460083</td>
      <td>50.000089</td>
    </tr>
    <tr>
      <th>4317</th>
      <td>858.839722</td>
      <td>38.559408</td>
    </tr>
    <tr>
      <th>4318</th>
      <td>850.602295</td>
      <td>43.006386</td>
    </tr>
    <tr>
      <th>4319</th>
      <td>848.962708</td>
      <td>29.822223</td>
    </tr>
    <tr>
      <th>4320</th>
      <td>622.935364</td>
      <td>30.287063</td>
    </tr>
    <tr>
      <th>4321</th>
      <td>845.083435</td>
      <td>30.828883</td>
    </tr>
    <tr>
      <th>4322</th>
      <td>425.538879</td>
      <td>40.715654</td>
    </tr>
    <tr>
      <th>4323</th>
      <td>428.923096</td>
      <td>41.930834</td>
    </tr>
    <tr>
      <th>4324</th>
      <td>866.067322</td>
      <td>22.541604</td>
    </tr>
    <tr>
      <th>4326</th>
      <td>858.878784</td>
      <td>29.318644</td>
    </tr>
    <tr>
      <th>4327</th>
      <td>433.984253</td>
      <td>42.114547</td>
    </tr>
    <tr>
      <th>4328</th>
      <td>868.553711</td>
      <td>42.111110</td>
    </tr>
    <tr>
      <th>4329</th>
      <td>851.664795</td>
      <td>30.006657</td>
    </tr>
    <tr>
      <th>4330</th>
      <td>334.160309</td>
      <td>42.255098</td>
    </tr>
    <tr>
      <th>4331</th>
      <td>851.653931</td>
      <td>29.446273</td>
    </tr>
    <tr>
      <th>4332</th>
      <td>855.022461</td>
      <td>35.600878</td>
    </tr>
    <tr>
      <th>4333</th>
      <td>435.255066</td>
      <td>42.096393</td>
    </tr>
    <tr>
      <th>4334</th>
      <td>342.619019</td>
      <td>36.602158</td>
    </tr>
    <tr>
      <th>4335</th>
      <td>350.144165</td>
      <td>38.426210</td>
    </tr>
    <tr>
      <th>4336</th>
      <td>868.355286</td>
      <td>31.084232</td>
    </tr>
  </tbody>
</table>
<p>4082 rows × 2 columns</p>
</div>




```python
width['width'] = 50 - width['length']
```


```python
width.head(5)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>keyman</th>
      <th>heading</th>
      <th>length</th>
      <th>width</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>432.257263</td>
      <td>49.999986</td>
      <td>0.000014</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>355.762207</td>
      <td>15.970360</td>
      <td>34.029640</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>289.011902</td>
      <td>18.414908</td>
      <td>31.585092</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>273.227387</td>
      <td>17.759665</td>
      <td>32.240335</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>273.227387</td>
      <td>12.740908</td>
      <td>37.259092</td>
    </tr>
  </tbody>
</table>
</div>




```python
width.to_csv('N:\\bandera\GIS\I_width.csv')
```


```python
street = pd.read_csv('N:\\bandera\GIS\Intersect_SOL.csv')
```


```python
street.count()
```




    keysol    7884
    id        7884
    x         7884
    y         7884
    id2       7884
    dtype: int64




```python
street.head(5)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>keysol</th>
      <th>id</th>
      <th>x</th>
      <th>y</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>4282</td>
      <td>1</td>
      <td>346398.6958</td>
      <td>6299570.390</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4298</td>
      <td>2</td>
      <td>346424.4173</td>
      <td>6299459.074</td>
    </tr>
    <tr>
      <th>2</th>
      <td>310</td>
      <td>3</td>
      <td>346428.9511</td>
      <td>6299455.496</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4290</td>
      <td>4</td>
      <td>346432.7133</td>
      <td>6299466.693</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4298</td>
      <td>5</td>
      <td>346431.7160</td>
      <td>6299459.526</td>
    </tr>
  </tbody>
</table>
</div>




```python
street['id2'] = street['id'] - 1
```


```python
streetm = pd.merge(street, street, left_on=['keysol','id'], right_on=['keysol','id2'],suffixes=('_L','_R'))
```


```python
streetm.count()
```




    keysol    53
    id_L      53
    x_L       53
    y_L       53
    id2_L     53
    id_R      53
    x_R       53
    y_R       53
    id2_R     53
    dtype: int64




```python
streetm.head(10)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>keysol</th>
      <th>id_L</th>
      <th>x_L</th>
      <th>y_L</th>
      <th>id2_L</th>
      <th>id_R</th>
      <th>x_R</th>
      <th>y_R</th>
      <th>id2_R</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>4304</td>
      <td>6</td>
      <td>346463.9767</td>
      <td>6299415.206</td>
      <td>5</td>
      <td>7</td>
      <td>346445.2618</td>
      <td>6299413.645</td>
      <td>6</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1209</td>
      <td>13</td>
      <td>345947.0774</td>
      <td>6298319.388</td>
      <td>12</td>
      <td>14</td>
      <td>345947.8926</td>
      <td>6298313.402</td>
      <td>13</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1995</td>
      <td>34</td>
      <td>345222.4566</td>
      <td>6297411.477</td>
      <td>33</td>
      <td>35</td>
      <td>345225.1428</td>
      <td>6297402.091</td>
      <td>34</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1995</td>
      <td>35</td>
      <td>345225.1428</td>
      <td>6297402.091</td>
      <td>34</td>
      <td>36</td>
      <td>345224.1446</td>
      <td>6297405.579</td>
      <td>35</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2763</td>
      <td>41</td>
      <td>345934.1163</td>
      <td>6296481.826</td>
      <td>40</td>
      <td>42</td>
      <td>345931.6774</td>
      <td>6296481.948</td>
      <td>41</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2779</td>
      <td>43</td>
      <td>345937.8146</td>
      <td>6296418.219</td>
      <td>42</td>
      <td>44</td>
      <td>345953.2547</td>
      <td>6296396.788</td>
      <td>43</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2779</td>
      <td>44</td>
      <td>345953.2547</td>
      <td>6296396.788</td>
      <td>43</td>
      <td>45</td>
      <td>345955.1165</td>
      <td>6296394.204</td>
      <td>44</td>
    </tr>
    <tr>
      <th>7</th>
      <td>3228</td>
      <td>48</td>
      <td>345398.2618</td>
      <td>6295822.095</td>
      <td>47</td>
      <td>49</td>
      <td>345390.1035</td>
      <td>6295821.736</td>
      <td>48</td>
    </tr>
    <tr>
      <th>8</th>
      <td>3228</td>
      <td>49</td>
      <td>345390.1035</td>
      <td>6295821.736</td>
      <td>48</td>
      <td>50</td>
      <td>345389.1513</td>
      <td>6295821.694</td>
      <td>49</td>
    </tr>
    <tr>
      <th>9</th>
      <td>4213</td>
      <td>60</td>
      <td>343955.9390</td>
      <td>6295342.177</td>
      <td>59</td>
      <td>61</td>
      <td>343941.3484</td>
      <td>6295349.939</td>
      <td>60</td>
    </tr>
  </tbody>
</table>
</div>




```python
streetdd = streetm.drop_duplicates(subset=['keysol'], keep='first')
```


```python
streetdd.head(10)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>keysol</th>
      <th>id_L</th>
      <th>x_L</th>
      <th>y_L</th>
      <th>id2_L</th>
      <th>id_R</th>
      <th>x_R</th>
      <th>y_R</th>
      <th>id2_R</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>4304</td>
      <td>6</td>
      <td>346463.9767</td>
      <td>6299415.206</td>
      <td>5</td>
      <td>7</td>
      <td>346445.2618</td>
      <td>6299413.645</td>
      <td>6</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1209</td>
      <td>13</td>
      <td>345947.0774</td>
      <td>6298319.388</td>
      <td>12</td>
      <td>14</td>
      <td>345947.8926</td>
      <td>6298313.402</td>
      <td>13</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2763</td>
      <td>41</td>
      <td>345934.1163</td>
      <td>6296481.826</td>
      <td>40</td>
      <td>42</td>
      <td>345931.6774</td>
      <td>6296481.948</td>
      <td>41</td>
    </tr>
    <tr>
      <th>9</th>
      <td>4213</td>
      <td>60</td>
      <td>343955.9390</td>
      <td>6295342.177</td>
      <td>59</td>
      <td>61</td>
      <td>343941.3484</td>
      <td>6295349.939</td>
      <td>60</td>
    </tr>
    <tr>
      <th>12</th>
      <td>4011</td>
      <td>69</td>
      <td>346793.3837</td>
      <td>6294881.864</td>
      <td>68</td>
      <td>70</td>
      <td>346794.5961</td>
      <td>6294867.106</td>
      <td>69</td>
    </tr>
    <tr>
      <th>13</th>
      <td>4089</td>
      <td>71</td>
      <td>346831.2854</td>
      <td>6294829.722</td>
      <td>70</td>
      <td>72</td>
      <td>346822.3382</td>
      <td>6294829.105</td>
      <td>71</td>
    </tr>
    <tr>
      <th>16</th>
      <td>4146</td>
      <td>714</td>
      <td>343778.9999</td>
      <td>6299404.156</td>
      <td>713</td>
      <td>715</td>
      <td>343765.4097</td>
      <td>6299402.890</td>
      <td>714</td>
    </tr>
    <tr>
      <th>17</th>
      <td>4308</td>
      <td>962</td>
      <td>347668.6180</td>
      <td>6299250.192</td>
      <td>961</td>
      <td>963</td>
      <td>347660.1217</td>
      <td>6299252.401</td>
      <td>962</td>
    </tr>
    <tr>
      <th>18</th>
      <td>554</td>
      <td>1014</td>
      <td>345258.3811</td>
      <td>6299125.721</td>
      <td>1013</td>
      <td>1015</td>
      <td>345250.9023</td>
      <td>6299118.073</td>
      <td>1014</td>
    </tr>
    <tr>
      <th>19</th>
      <td>754</td>
      <td>1309</td>
      <td>347321.0606</td>
      <td>6298883.114</td>
      <td>1308</td>
      <td>1310</td>
      <td>347317.1868</td>
      <td>6298882.140</td>
      <td>1309</td>
    </tr>
  </tbody>
</table>
</div>




```python
streetdd.to_csv('N:\\bandera\GIS\I_street.csv')
```


```python
streetdd.count()
```




    keysol    43
    id_L      43
    x_L       43
    y_L       43
    id2_L     43
    id_R      43
    x_R       43
    y_R       43
    id2_R     43
    dtype: int64




```python
street.head(5)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>keysol</th>
      <th>id</th>
      <th>x</th>
      <th>y</th>
      <th>id2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>4282</td>
      <td>1</td>
      <td>346398.6958</td>
      <td>6299570.390</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4298</td>
      <td>2</td>
      <td>346424.4173</td>
      <td>6299459.074</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>310</td>
      <td>3</td>
      <td>346428.9511</td>
      <td>6299455.496</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4290</td>
      <td>4</td>
      <td>346432.7133</td>
      <td>6299466.693</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4298</td>
      <td>5</td>
      <td>346431.7160</td>
      <td>6299459.526</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>




```python
street.groupby('keysol').size()
```




    keysol
    2       2
    3       2
    4       2
    5       2
    6       2
    7       2
    8       2
    9       2
    10      2
    11      2
    12      2
    13      2
    14      1
    15      2
    16      2
    17      2
    18      2
    19      2
    20      2
    21      2
    22      2
    23      2
    24      2
    25      2
    26      2
    27      2
    28      2
    29      2
    30      2
    31      2
           ..
    4306    2
    4307    2
    4308    4
    4309    2
    4310    2
    4311    2
    4312    3
    4313    3
    4314    3
    4315    2
    4317    2
    4318    2
    4319    2
    4320    2
    4321    2
    4322    2
    4323    1
    4324    1
    4325    1
    4326    2
    4327    1
    4328    2
    4329    2
    4330    1
    4331    1
    4332    2
    4333    1
    4334    2
    4335    1
    4336    2
    dtype: int64




```python
street.keysol.value_counts()
```




    2779    8
    4213    7
    4219    7
    651     6
    1995    6
    3228    6
    4089    6
    2763    6
    3602    5
    3114    5
    2400    5
    3575    5
    2749    5
    3592    5
    3463    5
    3586    5
    2568    5
    4298    5
    4255    5
    215     5
    889     5
    2754    5
    1930    5
    1866    5
    2554    5
    1778    5
    4091    5
    1974    5
    3585    4
    3301    4
           ..
    4151    1
    57      1
    2124    1
    51      1
    4153    1
    3553    1
    1680    1
    359     1
    299     1
    1596    1
    1604    1
    255     1
    1640    1
    4333    1
    4325    1
    1672    1
    2266    1
    207     1
    59      1
    3745    1
    171     1
    1780    1
    123     1
    4217    1
    3869    1
    3873    1
    4169    1
    2110    1
    1880    1
    4053    1
    Name: keysol, dtype: int64




```python
street.head(10)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>keysol</th>
      <th>id</th>
      <th>x</th>
      <th>y</th>
      <th>id2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>4282</td>
      <td>1</td>
      <td>346398.6958</td>
      <td>6299570.390</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4298</td>
      <td>2</td>
      <td>346424.4173</td>
      <td>6299459.074</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>310</td>
      <td>3</td>
      <td>346428.9511</td>
      <td>6299455.496</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4290</td>
      <td>4</td>
      <td>346432.7133</td>
      <td>6299466.693</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4298</td>
      <td>5</td>
      <td>346431.7160</td>
      <td>6299459.526</td>
      <td>4</td>
    </tr>
    <tr>
      <th>5</th>
      <td>4304</td>
      <td>6</td>
      <td>346463.9767</td>
      <td>6299415.206</td>
      <td>5</td>
    </tr>
    <tr>
      <th>6</th>
      <td>4304</td>
      <td>7</td>
      <td>346445.2618</td>
      <td>6299413.645</td>
      <td>6</td>
    </tr>
    <tr>
      <th>7</th>
      <td>395</td>
      <td>8</td>
      <td>346732.7473</td>
      <td>6299346.934</td>
      <td>7</td>
    </tr>
    <tr>
      <th>8</th>
      <td>4305</td>
      <td>9</td>
      <td>347313.1528</td>
      <td>6299344.467</td>
      <td>8</td>
    </tr>
    <tr>
      <th>9</th>
      <td>4308</td>
      <td>10</td>
      <td>347633.2580</td>
      <td>6299259.385</td>
      <td>9</td>
    </tr>
  </tbody>
</table>
</div>




```python
street = pd.read_csv('N:\\bandera\GIS\Intersect_SOL.csv')
```


```python
street.count()
```




    keysol    7884
    id        7884
    x         7884
    y         7884
    dtype: int64




```python
street.head()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>keysol</th>
      <th>id</th>
      <th>x</th>
      <th>y</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>4282</td>
      <td>1</td>
      <td>346398.6958</td>
      <td>6299570.390</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4298</td>
      <td>2</td>
      <td>346424.4173</td>
      <td>6299459.074</td>
    </tr>
    <tr>
      <th>2</th>
      <td>310</td>
      <td>3</td>
      <td>346428.9511</td>
      <td>6299455.496</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4290</td>
      <td>4</td>
      <td>346432.7133</td>
      <td>6299466.693</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4298</td>
      <td>5</td>
      <td>346431.7160</td>
      <td>6299459.526</td>
    </tr>
  </tbody>
</table>
</div>




```python
streetf = street.drop_duplicates(subset=['keysol'], keep='first')
```


```python
streetf.count()
```




    keysol    3803
    id        3803
    x         3803
    y         3803
    dtype: int64




```python
streetl = street.drop_duplicates(subset=['keysol'], keep='last')
```


```python
streetl.count()
```




    keysol    3803
    id        3803
    x         3803
    y         3803
    dtype: int64




```python
streetf.head()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>keysol</th>
      <th>id</th>
      <th>x</th>
      <th>y</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>4282</td>
      <td>1</td>
      <td>346398.6958</td>
      <td>6299570.390</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4298</td>
      <td>2</td>
      <td>346424.4173</td>
      <td>6299459.074</td>
    </tr>
    <tr>
      <th>2</th>
      <td>310</td>
      <td>3</td>
      <td>346428.9511</td>
      <td>6299455.496</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4290</td>
      <td>4</td>
      <td>346432.7133</td>
      <td>6299466.693</td>
    </tr>
    <tr>
      <th>5</th>
      <td>4304</td>
      <td>6</td>
      <td>346463.9767</td>
      <td>6299415.206</td>
    </tr>
  </tbody>
</table>
</div>




```python
streetl.head()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>keysol</th>
      <th>id</th>
      <th>x</th>
      <th>y</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>310</td>
      <td>3</td>
      <td>346428.9511</td>
      <td>6299455.496</td>
    </tr>
    <tr>
      <th>7</th>
      <td>395</td>
      <td>8</td>
      <td>346732.7473</td>
      <td>6299346.934</td>
    </tr>
    <tr>
      <th>13</th>
      <td>1209</td>
      <td>14</td>
      <td>345947.8926</td>
      <td>6298313.402</td>
    </tr>
    <tr>
      <th>64</th>
      <td>3839</td>
      <td>65</td>
      <td>344957.4524</td>
      <td>6295072.886</td>
    </tr>
    <tr>
      <th>66</th>
      <td>3869</td>
      <td>67</td>
      <td>344957.2454</td>
      <td>6295072.879</td>
    </tr>
  </tbody>
</table>
</div>




```python
sc = streetf.loc[streetf.keysol == 2]
print sc
```

        keysol  id            x            y
    79       2  80  343986.2673  6300072.831
    


```python
sc = streetl.loc[streetl.keysol == 2]
print sc
```

        keysol  id            x            y
    87       2  88  343994.1861  6300073.417
    


```python
streetr = pd.merge(streetf, streetl, on='keysol')
```


```python
streetr.count()
```




    keysol    3803
    id_x      3803
    x_x       3803
    y_x       3803
    id_y      3803
    x_y       3803
    y_y       3803
    dtype: int64




```python
streetr.to_csv('N:\\bandera\GIS\I_streett.csv')
```


```python

```
